# This Source Code Form is subject to the terms of the Mozilla Public
# License, v. 2.0. If a copy of the MPL was not distributed with this
# file, You can obtain one at http://mozilla.org/MPL/2.0/.


DEPTH		= ..

include $(DEPTH)/config/autoconf.mk

TST =

ifeq ($(TESTS),yes)
  TST = tst
endif

PREF_JS_EXPORTS = $(srcdir)/prefs/enigmail.js

COMPFILES = \
            enigmail.js \
            mimeDecrypt.js \
            mimeEncrypt.js \
            enigprefs-service.js \
            enigMsgCompFields.js

PREFFILES = prefs/enigmail.js

MODFILES = \
           app.jsm \
           armor.jsm \
           attachment.jsm \
           commandLine.jsm \
           configure.jsm \
           constants.jsm \
           data.jsm \
           decryption.jsm \
           decryptPermanently.jsm \
           dialog.jsm \
           encryption.jsm \
           enigmailCore.jsm \
           enigmailErrorHandling.jsm \
           enigmailFuncs.jsm \
           enigmailGpgAgent.jsm \
           enigmailProtocolHandler.jsm \
           events.jsm \
           execution.jsm \
           files.jsm \
           filters.jsm \
           fixExchangeMsg.jsm \
           glodaMime.jsm \
           glodaUtils.jsm \
           gpg.jsm \
           hash.jsm \
           httpProxy.jsm \
           installGnuPG.jsm \
           key.jsm \
           keyEditor.jsm \
           keyRing.jsm \
           keyserver.jsm \
           lazy.jsm \
           locale.jsm \
           log.jsm \
           mime.jsm \
           mimeVerify.jsm \
           os.jsm \
           passwordCheck.jsm \
           passwords.jsm \
           pipeConsole.jsm \
           prefs.jsm \
           promise.jsm \
           rules.jsm \
           streams.jsm \
           time.jsm \
           timer.jsm \
           trust.jsm \
           uris.jsm \
           verify.jsm \
           windows.jsm

all: deploy $(TST)

tst:
	$(MAKE) -C tests

deploy: $(PREFFILES) $(COMPFILES) $(MODFILES)
	$(DEPTH)/util/install -m 644 $(DIST)/components $(COMPFILES)
	$(DEPTH)/util/install -m 644 $(DIST)/defaults/preferences $(PREFFILES)
	$(DEPTH)/util/install -m 644 $(DIST)/modules $(MODFILES)


clean:
	$(DEPTH)/util/install -u $(DIST)/components $(COMPFILES)
	$(DEPTH)/util/install -u $(DIST)/defaults/preferences $(PREFFILES)
	$(DEPTH)/util/install -u $(DIST)/modules $(MODFILES)
