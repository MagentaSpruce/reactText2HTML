# reactText2HTML
This React app converts markdown text into HTML including image and link tags.

This app uses the npm package react-markdown: https://www.npmjs.com/package/react-markdown
***Check that page for syntax rules of markdown


A general walkthrough of the React code is given below:

After the initial file tree is set up, state value is assigned.
```React
  const [markdown, setMarkdown] = useState("# markdown preview");
```

Next the return is constructed.
```React
    <main>
      <section className="markdown">
        <textarea
          className="input"
          value={markdown}
          onChange={(e) => setMarkdown(e.target.value)}
        ></textarea>
        <article className="result">{markdown}</article>
      </section>
    </main>
  );
```  

Now that the general setup is complete, and the markdown is being diplayed in the text box and in the body, now the markdown inside the body needs to be converted into html instead from the markdown text. react-markdown is installed. Next the <ReactMarkdown> component is inserted.
```React
        <article className="result">
          <ReactMarkdown>{markdown}</ReactMarkdown>
        </article>
```

At this point the markdown is being converted into HTML.
***End walkthrough
