# Set GNUstep environment variables
# GNUSTEP_MAKEFILES = $(shell gnustep-config --variable=GNUSTEP_MAKEFILES)

include $(GNUSTEP_MAKEFILES)/common.make

APP_NAME = iTerm
iTerm_OBJC_FILES = main.m iTermKeyBindingMgr.m PseudoTerminal.m VT100Terminal.m iTermTerminalProfileMgr.m
iTerm_HEADER_FILES = iTermBookmarkController.h iTermGrowlDelegate.h
iTerm_RESOURCE_FILES = Profiles.plist iTerm_Framework.plist

include $(GNUSTEP_MAKEFILES)/application.make

# Clean target
clean::
    rm -rf obj $(APP_NAME).app

