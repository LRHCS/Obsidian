layout
```jsx
export default function RootLayout({ children }) {

  return (

    <html lang="en">

      <body>

        <nav className="text-sky-400 text-xl">

          <a href=".." className="mr-4">

            Home

          </a>

          <a href="about">About</a>

        </nav>

        <div className="mx-10 my-4">{children}</div>

      </body>

    </html>

  );

}
```