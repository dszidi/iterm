# Set the GNUstep environment variables
# GNUSTEP_MAKEFILES = $(shell gnustep-config --variable=GNUSTEP_MAKEFILES)
CC = clang
CFLAGS = -Wall -g -O2 -fobjc-exceptions -I. -fblocks $(shell gnustep-config --objc-flags)
LDFLAGS = $(shell gnustep-config --base-libs) -lgnustep-base -lgnustep-gui -lobjc

include $(GNUSTEP_MAKEFILES)/common.make

# Define application name and source files
APP_NAME = iTerm
iTerm_OBJC_FILES = main.m iTermKeyBindingMgr.m PseudoTerminal.m VT100Terminal.m iTermTerminalProfileMgr.m
iTerm_HEADER_FILES = iTermBookmarkController.h iTermGrowlDelegate.h
iTerm_RESOURCE_FILES = Profiles.plist iTerm_Framework.plist

include $(GNUSTEP_MAKEFILES)/application.make

# Rules for building the application
$(APP_NAME): $(iTerm_OBJC_FILES)
	$(CC) $(CFLAGS) -o $(APP_NAME) $(iTerm_OBJC_FILES) $(LDFLAGS)

# Clean target
clean::
	rm -rf obj $(APP_NAME).app

