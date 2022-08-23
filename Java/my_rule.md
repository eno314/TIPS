# Java's my coding rule

## How to use NULL

- Arguments, Return values and Member variables should not be Null as much as possible. (引数、返り値、メンバ変数は可能な限りNullにならないようにする)
- Use 'Optional' when we have to return value which can be Null. (返り値にNullの可能性がある値を返す必要がある場合は、Optionalを使う)
- Use Optional only at Return value and Local variables, don't use it at Arguments and Member variables, because it's not Serializable. (OptionalはSerializableじゃないので返り値やローカル変数でだけ使用する。引数やメンバ変数には使わない。)
- Use Nullable annotation When we have to define Arguments and Member variables which can be Null. (Nullになる可能性がある引数やメンバ変数を定義しなければいけない場合は、Nullableのアノテーションを使う)
