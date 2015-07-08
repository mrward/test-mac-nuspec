Three test .nuspec files that check nuget pack works on the Mac.

To test:

 1. Open a terminal.
 2. cd into the src directory inside this repository.
 3. Run `nuget pack NameOfNuSpec.nuspec` for each .nuspec file

**absolute-path.nuspec**

Note that the absolute path in the file may need to be changed so it matches your path. Change it before testing it.

    <file src="/full/path/to/github/repo/test-mac-nuspec/src/lib/Net40/*.*" target="lib/Net40" />

This will fail with nuget since it uses an absolute path.

**relative-path.nuspec**

This will work.

**parent-relative-path.nuspec**

This will fail with nuget since it uses a relative path which is in a directory above the current working directory.