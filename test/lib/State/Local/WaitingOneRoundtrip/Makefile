# SPDX-FileCopyrightText: 2019 Serokell <https://serokell.io>
#
# SPDX-License-Identifier: MPL-2.0

.PHONY: test/lib/State/Local/WaitingOneRoundtrip/roundtripTest.fif
test/lib/State/Local/WaitingOneRoundtrip/roundtripTest.fif: test/lib/State/Local/WaitingOneRoundtrip/roundtripTest.asm.gen
	$(fift_compiler)  -I$(fift_lib):src/lib $@

test/lib/State/Local/WaitingOneRoundtrip/roundtripTest.asm.gen: src/lib/Util.fc src/contract/errors.fc src/lib/State/Local/StateTags.fc src/lib/State/Local/WaitingOne.fc test/lib/State/Local/WaitingOneRoundtrip/roundtripTest.fc
	$(func_compiler) -P -o$@ $(func_lib) $^
