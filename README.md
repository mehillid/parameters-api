Example usage
```java
static KeyParam<Integer> VALUE = KeyParam.of("value", 2);
static KeyParam<String> HOST = KeyParam.of( "host", "localhost", "this is host address");
static KeyParam<String> PASSWORD = KeyParam.ofSecret("password", "");

public TestPlugin() {
    super(VALUE, HOST, PASSWORD);
}

@Override
public void onEnable() {

}


@Override
public void run(Context ctx) {
  String host = ctx.param(HOST);
}
```
