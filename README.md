# Managed package installation tool

Steps to install managed packages:

1. Create a build.properties file from build.properties.template
2. Fill in the sf.username/sf.password/sf.token properties, change the login host if necessary
3. Modify the versions of packages in build.xml (if necessary). 
   Example:
   ```xml
   <installPackage namespace="mypkgnamespace" version="1.2.3" username="${sf.username}" password="${sf.password}${sf.token}" packagePassword="" />
   ```
   Namespace should be equal to package prefix.

   Version should be _major.minor.patch_

   Package password should be set if a package is password protected.

4. Run the script by executing _ant install_.
5. Grab a coffee and wait for the packages to be installed.

