* Download [Pixman 0.32.8](http://cairographics.org/releases/pixman-0.32.8.tar.gz)
* Get project files from [Chun-Wei's bug](https://bugs.freedesktop.org/attachment.cgi?id=58220)
* In `build\win32\vc14\pixman.props`, replace:
	* `<PixmanEtcInstallRoot>..\..\..\..\vs10\$(PlatformName)</PixmanEtcInstallRoot>` with `<PixmanEtcInstallRoot>..\..\..\..\..\..\gtk\$(PlatformName)</PixmanEtcInstallRoot>`
	* `<CopyDir>$(PixmanEtcInstallRoot)</CopyDir>` with `<CopyDir>..\..\..\..\pixman-rel</CopyDir>`
* In `build\win32\vc14\pixman.props`, add to `PixmanDoInstall`:
	* `copy $(SolutionDir)$(Configuration)\$(Platform)\bin\*.exe $(CopyDir)\bin`
	* `copy $(SolutionDir)$(Configuration)\$(Platform)\bin\*.pdb $(CopyDir)\bin`
* Build `build\win32\vc14\pixman.vcxproj` and `build\win32\vc14\install.vcxproj`
