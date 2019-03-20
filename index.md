## Golang 

### Structure
Package structure should look as follows:

```
/package
    doc.go (package documentation)
    /handler
        doc.go (package documentation)
        handler.go (interface)
        /default
            handler.go (implementation) 
    /recordkeeper
        doc.go (package documentation)
        recordkeeper.go (interface)
        /adaptors
        /exceptions
            errors.go (custom errors for this package)
        /mongo
            recordkeeper.go (implementation)
```

### JsonRPC

How to register JsonRPC adaptors
```golang
if err = apiServer.RegisterService(&requestForFundsHandlerJsonRpcAdaptor, "RequestForFunds-Handler"); err != nil {
	log.Fatal("Failed to register RequestForFunds-Handler")
}
```
Take note of the structure for the `name` parameter `"RequestForFunds-Handler"`

[Link](url) and ![Image](src)

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

You can use the [editor on GitHub](https://github.com/andile-innovation/standards/edit/master/index.md) to maintain and preview the content of this website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
