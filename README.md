# Report Scripts

This is a project where I store useful reporting scripts.

I :heart: automating reports!

Requirements:
- Python 3

## Obsidian Converters

The Obsidian default syntax for images is the following:

```sh
![[<generated-name>]]
```

> Note: Obsidian syntax can be changed as explained [here](https://forum.obsidian.md/t/change-markdown-syntax-image/13253).

### Obsidian to Markdown

The obsidian default syntax for images is not correct for markdown files. You can easily fix your report by using `obsidian-to-markdown`:

```sh
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_markdown.py -f ..\examples\obsidian.md -i './' -o new_file.md
[+] New pattern: ![syntax](/images/htb/shared/syntax)
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_markdown.py -f ..\examples\obsidian.md -i '../images/' -o new_file.md
[+] New pattern: ![syntax](/images/htb/shared/syntax)
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_markdown.py -f ..\examples\obsidian.md -i '.' -o new_file.md         
[+] New pattern: ![syntax](/images/htb/shared/syntax)
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_markdown.py -f ..\examples\obsidian.md -i '../images' -o new_file.md 
[+] New pattern: ![syntax](/images/htb/shared/syntax)
```

The created file looks like this:

```sh
Change this image syntax:

![syntax](../examples/syntax)

```

### Obsidian to Hugo

The obsidian default syntax for images is not compatible with Hugo either. This can be fixed by using `obsidian-to-hugo`:

```sh
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_hugo.py -f ..\examples\obsidian.md -i '../examples/' -o new_file.md
[+] New pattern: ![syntax](../examples/syntax 'syntax')
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_hugo.py -f ..\examples\obsidian.md -i '../examples' -o new_file.md 
[+] New pattern: ![syntax](../examples/syntax 'syntax')
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_hugo.py -f ..\examples\obsidian.md -i '.' -o new_file.md
[+] New pattern: ![syntax](./syntax 'syntax')
PS C:\Tools\ReportScripts\obsidian> python .\obsidian_to_hugo.py -f ..\examples\obsidian.md -i './' -o new_file.md
[+] New pattern: ![syntax](./syntax 'syntax')
```

The created file looks like this:

```sh
Change this image syntax:

![syntax](../examples/syntax 'syntax')

```

# ToDo

- [ ] MS Word Macros or Scripts
- [ ] Markdown Scripts