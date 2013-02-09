# How to install the AssetJet Python Environment with scientific packages on a Mac (Mountain Lion)

## [1] Xcode
* Install Xcode from the AppStore.
* Run it, then select "Create a new Xcode project"
* Under Xcode/Preferences, install the Command Line Tools. You may have to repeat the last step after every Xcode update. 

## [2] Homebrew
* Install Homebrew by pasting the following at a Terminal prompt:
ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
* Run "brew update"
* Run "brew doctor" and google/fix all the messages
* You may have to edit the path order "sudo vi /etc/paths" to make sure that "usr/local/bin" appears before "/usr/bin" (google vim commands)

## [3] Python
`brew install python --framework --universal`

## [4] Optional: virtualenv/virtualenvwrapper
* using virtualenv, the installation of the packages can be automated with a bootstrap script
pip install virtualenv
pip install virtualenvwrapper
source /usr/local/share/python/virtualenvwrapper.sh
mkvirtualenv <virtualenvname>
workon <virtualenvname>

## [5] Packages
* Some of the packages will install additional packages their are depending on
* Note that for numpy "--devel" or "--HEAD" is needed to get 1.7rc

brew tap samueljohn/python
brew install numpy --devel
brew install scipy
brew install pyside
pip install matplotlib
pip install sphinx
pip install nose
pip install spyder
pip install pyramid
pip install pandas
pip install sqlalchemy
pip install web.py
pip install esky
pip install lxml

## [6] Upgrades
brew upgrade <packagename>
pip install <packagename> --upgrade

## [7] Uninstalls
brew uninstall <packagename>
pip uninstall <packagename>
rmvirtualenv <virutalenvname>

## [8] Links/Sources
http://mxcl.github.com/homebrew
http://www.virtualenv.org
http://www.pip-installer.org
http://www.thisisthegreenroom.com/2011/installing-python-numpy-scipy-matplotlib-and-ipython-on-lion
https://github.com/mxcl/homebrew/wiki/Homebrew-and-Python
https://github.com/samueljohn/homebrew-python