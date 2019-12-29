---
layout: post
---
Hello world for the $$n+1$$ times. This post will serve as a repo for troubleshooting blogging problems.

### Convert between different sources
HTML to MarkDown: `pandoc input.html -o output.md --parse-raw`

### Markdown editors
[`MarkdownEditting`](https://github.com/SublimeText-Markdown/MarkdownEditing) for Sublime Text


```r
library(knitr)
```

```
## Warning: package 'knitr' was built under R version 3.3.2
```

```r
set.seed(123)
rnorm(5)
```

```
## [1] -0.56047565 -0.23017749  1.55870831  0.07050839  0.12928774
```

Does **knitr** work with Python? Use the chunk option `engine='python'`:


```python
x = 'hello, python world!'
print(x)
print(x.split(' '))
```

```
## hello, python world!
## ['hello,', 'python', 'world!']
```

{% raw  %}
{% highlight c++ %}  <br/> code code code <br/> {% endhighlight %}{% endraw %}

Produces something like this: 

{% highlight c++ %}

int main(int argc, char const *argv[])
{
	string myString;

	cout << "input a string: ";
	getline(cin, myString);
	int length = myString.length();
	
	char charArray = new char * [length];

	charArray = myString;
	for(int i = 0; i < length; ++i){
		cout << charArray[i] << " ";
	}
	
	return 0;
}

{% endhighlight %}
