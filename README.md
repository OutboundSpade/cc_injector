<h1 align='center'> CC injector </h1>
<h3 align='center'> C compiler code injector </h3>

## DISCLAIMER
For educational purposes only! See [LICENSE](LICENSE) for more information.

## Usage
### CLI
Use it just as you would gcc
```
./cc_injector [file]
```

```
./cc_injector [file] -o [output]
```
... etc

### Modifying Variables

In the `cc_injector` file, 2 variables are intended for modification:
`CC` and `TMP_PATH`.

`CC` - path/name of your "real" c compiler (ex. gcc, clang)

`TMP_PATH` - path of the directory where the payload & temparary object header file is stored

### Structure

`cc_injector` - injector

`tmp_dir/` - default `TMP_PATH`

`tmp_dir/payload.c` - payload to be injected

`tmp_dir/other.h` - temparary object header file

## Example

```
./cc_inject example.c && ./a.out
```
The above will result in the following output:
```
Ha ha! code injected!
Hello World!
```
