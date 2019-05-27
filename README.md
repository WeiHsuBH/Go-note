# Go-note
记录go的一些姿势

## []int to []interface{}
go语言的interface也是一种类型，实现了一个interface的所有的方法，即实现了该interface，在某些应用场景中，需要将普通切片转换成interface的切片，直接使用.([] interface)则会报错，如下：
```
s := make([]interface{}, len(b))
for i, v := range b {
	s[i] = v
}
```
