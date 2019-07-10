# anyenv-install

Default install manifests for [anyenv](https://github.com/anyenv/anyenv).



## Example

For example, `rbenv`:

```
install_env https://github.com/rbenv/rbenv.git"
install_plugin ruby-build https://github.com/rbenv/ruby-build.git
```

It will create these directories after `anyenv install rbenv`:

```
/Users/<username>/.anyenv/envs
└── rbenv
    └── plugins
        └── ruby-build
```



## Specification

Install manifest is just a shell script. You have to add at least one line using `install_env` function. Also, you can install its plugins by using `install_plugin` function.

### `install_env`
Install **env into `ANYENV_ENVS_ROOT`. It will create a directory using the same name of the manifest file.

#### Usage

```
install_env git_url [git_ref]
```



### `install_plugin`

Install a plugin under `plugins` directory inside the env directory which is created by `install_env`. It will create a directory named by specified `destination`.

#### Usage
````
install_plugin destination git_url [git_ref]
````



#### Credit

* [anyenv-install](https://github.com/anyenv/anyenv-install)

