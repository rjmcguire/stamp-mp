# ==============================================================================
#
# Makefile
#
# ==============================================================================


include ../common/Defines.common.mk
include ./Defines.common.mk
include ../common/Makefile.$(TARGET)


.PHONY: test_data
test_data: CFLAGS += -DTEST_DATA -O0
test_data:
	$(CC) $(CFLAGS) data.c sort.c net.c $(LIB_SRCS) -o $@

.PHONY: test_net
test_net: CFLAGS += -DTEST_NET -O0
test_net:
	$(CC) $(CFLAGS) net.c $(LIB_SRCS) -o $@

.PHONY: test_adtree
test_adtree: CFLAGS += -DTEST_ADTREE -O0
test_adtree:
	$(CC) $(CFLAGS) adtree.c data.c net.c sort.c $(LIB_SRCS) -o $@

.PHONY: test_learner
test_learner: CFLAGS += -DTEST_LEARNER -O0
test_learner:
	$(CC) $(CFLAGS) learner.c sort.c adtree.c data.c net.c $(LIB_SRCS) -lm -o $@

# ==============================================================================
#
# Makefile
#
# ==============================================================================

