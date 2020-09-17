# blog.noahkernis.com

These are notes on writing posts. 

For usage, see [Hugo](https://gohugo.io/).

## Shortcodes

### Figure and Images

```go
{{< figure src="https://s3.amazonaws.com/media.noahkernis.com/images/life_is_weird.gif" alt="description of image" caption="[ title ]" >}}
```

### Code

```go
{{< code language="javascript" title="code code code" line-numbers="true">}}
function carl() {
	console.log("carla")
}
{{< /code >}}
```