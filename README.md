# Kubectl plugin - helm

This ```kubectl``` supports the following custom ```helm``` command.

## Custom helm commands

```
kubectl helm-diff WHAT [--code] --release1 RELEASE1 --revision1 R1 [--namespace1 NAMESPACE1] --release2 RELEASE2 --revision2 R2 [--namespace2 NAMESPACE2]
```

where WHAT is:

comma separated (no space before or after commas) set of some of these options all, hooks, manifest, notes, values, templates

--code option specifies to use VSCode to show the diff

## Building

```
npm install
npm run pkg
```

## Use it locally

- Add the ```dist/YOURPLATFORM/bin``` folder to your PATH variable.

- Confirm that ``kubectl``` is able to see the plugin by doing the following:

```
kubectl plugin list
```

- Invoke the plugin as shown above.


## Installation of the plugin

Once the plugin is available on [krew-index](), install it like this:

```
kubectl krew install helm-diff
```
