this is like an index.html, defines the looks
```jsx
import Image from "next/image";

  

export default async function MovieDetail({ params }) {

  const poster_image_path = "https://image.tmdb.org/t/p/original";

  const { movie } = params;

  const data = await fetch(

    `https://api.themoviedb.org/3/movie/${movie}?api_key=${process.env.API_KEY}`

  );

  const res = await data.json();

  return (

    <div>

      <h1 className="text-5xl ">{res.title}</h1>

      <h2>{res.release_date}</h2>

      <Image

        className="my-12"

        src={poster_image_path + res.backdrop_path}

        width={1000}

        height={1000}

      />

      <p>{res.overview}</p>

    </div>

  );

}
```