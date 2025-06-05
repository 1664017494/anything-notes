# CSS

# 优化字体和样式

# Layouts

# 导航

## 导航标签
用`<link>` 标签替换`<a>` 标签

- a标签使用的是原始的页面跳转，会刷新整个页面
- Link标签是部分刷新，只会更新需要更新的子组件

> 注意：为了提高导航体验，Next.js 会自动按路由段拆分您的应用程序。这与传统的 React SPA 不同，传统 SPA 在初始加载时会加载应用程序的所有代码。
>
> 这样做的好处：
> 1. 代码隔离，减小刷新的区域，同时提高安全性（某个内容报错，其余的区域仍正常运行）
>
> 此外，在生产环境中，每当 <Link> 组件出现在浏览器的视口中时，Next.js 会自动在后台预取链接路由的代码。当用户点击链接时，目标页面的代码将在后台已经加载，这就是使页面过渡几乎瞬间完成的原因！


## usePathname

用以下方式可以获取pathname，用于确定哪个Link标签是激活的状态
```tsx
import { usePathname } from 'next/navigation';

const pathname = usePathname()
```

# 获取数据

## API、ORM、SQL
API 是你的应用程序代码和数据库之间的中间层。

- 如果你使用提供 API 的第三方服务。
- 如果你从客户端获取数据，你希望有一个在服务器上运行的 API 层，以避免将数据库秘密暴露给客户端。

## Server Component

默认情况下，Next.js 应用程序使用 React Server Components。使用 Server Components 获取数据是一种相对较新的方法，使用它们有一些好处：

Server Components 支持 promises，为异步任务（如数据获取）提供了更简单的解决方案。你可以使用 async/await 语法，而无需使用 useEffect、useState 或数据获取库。
Server Components 在服务器上执行，因此你可以将昂贵的数据获取和逻辑保留在服务器上，并仅将结果发送到客户端。

## 网络瀑布


## 获取数据