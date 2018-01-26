# Stuecheli, Jeff - POWER9 - 2017-01-26

Time markers in a POWER9 chip webinar from January, it has a fair amount of detailed information.
The [YouTube video](https://www.youtube.com/watch?v=eBvscMLVLEU) appears to be down at the moment, apparently unintentionally, but the slides and video can be downloaded at the [AIX Virtual User Group's webpage][0], the slides can be found under the heading "January 26, 2017 - POWER9 - Jeff Stuecheli", while the video files are listed by a bare [index page at public.dhe.ibm.com][1].

### Time markers
0:00 intro/VUG announcements - Jill Armstrong  
2:59 presentation start - Jeff Stuecheli (chip development)  
3:54 POWER roadmap  
7:22 POWER9 markets  
11:15 core design - SMT8 vs SMT4  
14:20 core execution slice microarchitecture  
17:43 pipeline improvements  
19:30 core diagram slide - SMT4 core  
21:00 memory attachment - SO vs SU  
25:08 common features  
32:12 SO/SU SMT4/SMT8 matrix  
34:15 performance vs POWER8  
35:53 POWER ISA 3 instructions  
38:42 POWER 9 logical view - interconnects/throughput  
39:57 25 Gb/s signaling for SMP, Open CAPI, NVLink 2  
41:10 16 socket topology - probably called 980  
42:23 interrupt design  
44:18 accelerators  
47:09 accelerator connection types  
49:38 progression - PCIe3 → PCIe4 → NVLink → Open CAPI  
50:42 POWER9 ecosystem  
51:30 Open CAPI  
55:01 members  
56:12 Open CAPI 3 features  
57:24 virtual addressing  
57:55 attached memory et al.  
59:21 end of slides  
1:00:01 Q&A start  
1:00:39 Q: performance vs POWER8 - graph same for SMT4 compared as for SMT8 compared?  
1:02:34 Q: can different chip types be mixed  
1:03:26 Q: chip speeds  
1:04:33 Q: ISA affecting AIX version compatibility  
1:05:51 Q: live partition mobility  
1:06:36 Q: number of 25 Gb/s links  
1:08:10 Q: SMT4 vs SMT8, Linux vs AIX  
1:10:29 Q: POWER9 vs x86  
1:12:39 Q: DW on chart - looking for slide  
1:14:04 – relevant slide for above found  
1:14:36 Q: are charts/slides confidential  
1:15:17 announce NDA session in Orlando  
1:16:45 Q: Java improvements  
1:17:43 Q: Open CAPI attached memory uses  
1:19:20 Q: PCIe4 adapters/uses  
1:21:34 Q: accelerator effect on rPerf  
1:23:17 Q: will it run Windows  
1:23:36 Q: SAP HANA offerings, upgrade path  
1:24:03 Q: dynamic SMT  
1:24:56 threading changes from POWER8  
1:25:45 end remarks

### Interesting Notes
#### Intended Use of Chips (slide 10)

||SMT4|SMT8
-|-|-
**SO**|PowerNV|dual-socket PowerVM
**SU**||multi-socket PowerVM

The SMT4 column is labelled "Linux ecosystem", but is talking about PowerNV; saying Linux is actually a bit confusing since you can run Linux under PowerVM.

I wonder why PowerVM benefits from SMT8 where Linux does not?

#### 25 Gb/s optical connexion (slide 14)
in addition to PCIe4 (which carries CAPI 2) there is also optical 25 Gb/s connection used by Open CAPI, NVLink 2, and SMP interconnect; cool.

[0]: https://www.ibm.com/developerworks/community/wikis/home?lang=en#/wiki/Power%20Systems/page/AIX%20Virtual%20User%20Group%20-%20USA
[1]: https://public.dhe.ibm.com/systems/power/community/aix/Central-VUG-Replays/
