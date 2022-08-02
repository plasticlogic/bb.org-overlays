# Make a dtbo file

## Step 1: Pre-process dts file

```console
debian@beaglebone:~/bb.org-overlays$ gcc -I include -E -nostdinc -undef -D__DTS__ -x assembler-with-cpp -o /tmp/PL-FALCON-4_1_5-00A0.dts.processed src/arm/PL-FALCON-4_1_5-00A0.dts
```

## Step 2: Compile processed dts file

```console
debian@beaglebone:/tmp$ dtc -I dts -O dtb -o PL-FALCON-4_1_5-00A0.dtbo PL-FALCON-4_1_5-00A0.dts.processed
```