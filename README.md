# Various STM8 (and maybe STM32 in the future) repos

## Directory structure

* app/
  * Application specific code and Makefile. Launch make in the application's directory to compile it
* toolchain/
  * Makefile includes for compiler environment variables
  * Include from application Makefile to set CC, LD, etc..
* lib/
  * Various 3rd party components, such as STM8 SPL

## Projects

### parking-timer


