
In Next.js and React Router, searchParams (short for "search parameters") refers to the query string parameters in the URL, often used to pass information from one page to another without having to set up state or rely on form data. For example, in the URL:

Accessing Search Parameters in Next.js
In Next.js, you can use searchParams when working in server components (like in a page or route handler file) to directly access these URL parameters. Here’s how you might use it in a Next.js app router:

tsx

// In a Next.js server component (e.g., app/page.tsx)
export default function Page({ searchParams }) {
    const name = searchParams.get('name'); // "hariprasath"
    const age = searchParams.get('age'); // "25"
    
    return (
        <div>
            <p>Name: {name}</p>
            <p>Age: {age}</p>
        </div>
    );
}
Here:

searchParams.get('name') retrieves the value associated with the name parameter.
This approach only works in the Next.js app directory.