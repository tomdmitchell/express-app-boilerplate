# Express App Boilerplate

https://kentcdodds.com/blog/how-i-structure-express-apps

### Build Script
--delete-dir-on-start ensures that we don't have old files hanging around between builds

--out-dir dist indicates where we want the compiled version of the files to be saved

--copy-files indicates that files that are not compiled should be copied instead (useful for .json files for example)

--ignore \"**/__tests__/**,**/__mocks__/**\" is necessary so we don't bother compiling any test-related files because we don't need those in production anyway

--no-copy-ignored since we're not compiling the ignored files, we want to indicate that we'd also like to not bother copying them either (so this disables --copy-files for the ignored files).