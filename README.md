Do you need to create a Debian `.deb` package and you don't know how?

This is a simple way to create a rudimental package that works on any Debian based distro

Start with editing the content of `code/DEBIAN/control` file

Outside of `code` add any file (directory and subdirectory) that you need to add to the root filesystem, like you see here in the `usr` directory

Then create your `.deb` package like this:

```
cd <root folder of this project>
project_dir=$(pwd)
package_dir="$project_dir/code"
dpkg --build $package_dir $project_dir
```
