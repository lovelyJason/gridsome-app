# gridsome使用

## 集合(Collections)

gridsome中的集合主要起到两个作用,一方面是重载数据,另一方面,gridsome会根据集合中的节点模板预渲染成页面

如果你想预渲染出动态的数据,需要借助`Data sources`转换为`Collections`,这个`Data sources` 可以是wordpress等cms容器,markdown文件数据,api接口数据, `Collections`中有`Post`, `Tag`等集合,最后再转换成`Nodes`,每Node可能对应的是一个文章

### 添加集合的方式

- 在gridsome.config.js通过`sourcer plugins`插件集成数据
- 在gridsome.server.js中,使用数据存储api创建集合

通过`jsonplaceholder`可以模拟数据接口,以便学习和测试使用

### 获取集合中的数据

每个集合会被添加到GraphQl schema中,且会以两个字段的形式,如你有一个`Post`的集合,schema中会有post和allPost两个字段,分别用于查询单个文章和所有文章列表

## 页面中查询GraphQL

- page和模板页中使用`<page-query>`写查询语句
- 组件中使用`<static-query>`写查询语句

如以下语句,查询到所有文章列表,并取到id和title字段,将查到的结果起个别名叫posts

```vue
<page-query>
  query {
    posts: allPost {
      edges {
        node {
          id
          title
        }
      }
    }
  }

</page-query>
```

此时,posts会被注入到computed中的$page属性上

你可以通过传递参数查询特定记录的信息
```vue
# $id是graphQL的变量名,必须以$开头, `ID!`表示这是一个数据类型,且为ID类型,不能为空
<page-query>
  query ($id: ID!) {
    post (id: 2) {
      id
      title
    }
  }

</page-query>
```

注意: 如果你想在浏览器看到预渲染的内容,开发环境下是看不到效果的,需要进行打包

## 使用模板渲染节点页面

假设你现在需要针对上面创建的Post集合建立路由以及路由下的模板,在src/templates下创建文件{Collection}.vue,或者你也可以通过gridsome.config.js指定具体配置.当没有具体的组件指向时,模板会被调用

```javascript
# gridsome.config.js

module.exports = {
  templates: {
    Post: [
      {
        path: '/posts/:id',   // id要和server.js中的字段一致
        component: './src/templates/Post.vue'
      }
    ]
  }
}

```

此时访问/posts/:id可以访问到Post.vue对应的页面


## strapi与gridsome集成

首先再strapi中开启graphql的支持
```bash
npm run strapi install graphql
```

使用插件@gridsome/source-strapi即可集成strapi和gridsome


