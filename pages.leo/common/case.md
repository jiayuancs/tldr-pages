# case [modified]

> Branch based on the value of an expression.
> More information: <https://manned.org/case>.

- 语法格式，注意每个程序段后面都要有 `;;` 以表示段落结束：

```
case {{$variable}} in
  {{pattern1}})
    {{command_block1}}
    ;;
  {{pattern2}})
    {{command_block2}}
    ;;
  {{pattern3}})
    {{command_block3}}
    ;;
  *)
    {{command_block4}}
    ;;
esac
```

- Match a variable against string literals to decide which command to run:

`case {{$tocount}} in {{words}}) {{wc -w README}}; ;; {{lines}}) {{wc -l README}}; ;; esac`

- Combine patterns with |, use * as a fallback pattern,
- [wW]|words 匹配：w 或 W 或 words

`case {{$tocount}} in {{[wW]|words}}) {{wc -w README}}; ;; {{[lL]|lines}}) {{wc -l README}}; ;; *) {{echo "what?"}}; ;; esac`
