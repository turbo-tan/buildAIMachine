# Build a dual RTX 3090 AI workstation

**UK used-market price snapshot: 21 November 2026.**

Six platform options, from DDR3 Xeons and Intel X299 to dual PCIe 4.0 x16 Threadripper, with an estimated 128 GB of host RAM. Graphics cards are excluded from platform totals.

[Illustrated HTML version](https://turbo-tan.github.io/buildAIMachine/dual_3090_uk_platform_guide.html) | [Corrections and suggestions](https://github.com/turbo-tan/buildAIMachine/issues/new/choose)

This Markdown companion transcribes the supplied HTML guide. Prices below are a dated snapshot, not live quotations. Source notes distinguish asking prices, completed listings, owner-reported purchases and estimates.

## GPU and memory starting points

| Component | Capacity / rated power | Price reference |
|---|---|---|
| One RTX 3090 Founders Edition | 24 GB VRAM; 350 W rated board power | GPU cost excluded |
| Two RTX 3090 Founders Edition cards | 48 GB total; 700 W combined rated GPU power | Memory is not automatically pooled |
| Used 128 GB DDR3 ECC RDIMM | 8 x 16 GB | About GBP 138 asking |
| Used 128 GB DDR4-3200 UDIMM | 4 x 32 GB Corsair | About GBP 594 asking |

Rated power is not measured wall-socket consumption.

## Platform cost and compatibility

All prices are GBP. System budgets include motherboard, CPU, 128 GB total RAM and a suitable PSU. They **exclude GPUs, case, storage, cooler and shipping**.

| Platform / CPU | GPU PCIe wiring | 128 GB memory budget | Board + CPU | PSU: one / two GPUs | Estimated system budget |
|---|---|---|---|---|---|
| X99 / Xeon E5-2678 v3, 12 cores | PCIe 3.0 x16/x16, board-dependent | DDR3 ECC RDIMM, 8 x 16 GB: 140-210; selected DDR3-capable boards only | 90-210; board 60-175, CPU 23-36 | 850 W / 1200-1500 W | 420-720; two-GPU configuration |
| X299 / Core i9-10900X, 10 cores / 20 threads | PCIe 3.0 x16/x16 with a suitable 44/48-lane CPU and board | DDR4-3200 UDIMM, 4 x 32 GB: 550-700; quad-channel, XMP may be needed | 390-560; example bundles include 32 GB | 850 W / 1200-1500 W | 1140-1590; two GPUs, separately budgeted 128 GB |
| B550 / Ryzen 5950X, 16 cores | PCIe 4.0 x16; second slot often chipset x4 | DDR4-3200 UDIMM, 4 x 32 GB: 550-700 | 330-520; board 60-120, CPU estimated | 850 W / not budgeted for dual GPUs here | 960-1350; one-GPU configuration |
| X570 / Ryzen 5950X, 16 cores | PCIe 4.0 x8/x8 only on supported boards | DDR4-3200 UDIMM, 4 x 32 GB: 550-700 | 420-710; x8/x8 board 150-310 | 850 W / 1200-1500 W | 1160-1710; two-GPU configuration |
| TRX40 DESIGNARE / Threadripper 3960X, 24 cores | PCIe 4.0 x16/x16; verify exact slots and four-slot NVLink bridge fit | DDR4-3200 UDIMM, 4 x 32 GB: 550-700; reuse owned RAM for no extra purchase | 800 paid: board 390 + CPU 410 | 1000 W / 1500-1600 W | 1550-1830; two GPUs, separately budgeted 128 GB |
| WRX80 / Threadripper PRO 5955WX, 16 cores | PCIe 4.0 x16/x16; up to 128 CPU lanes | DDR4 ECC RDIMM, 8 x 16 GB: 370-650; 2400-3200 speed varies | 1900-2300; board alone seen at 1390 | 1000 W / 1500-1600 W | 2490-3300; two-GPU configuration |

PCIe 3.0 x16 and PCIe 4.0 x8 have approximately comparable link bandwidth. This is **not a training-throughput prediction**. Actual two-GPU wiring depends on the exact CPU, motherboard, slot pair and other installed devices.

Some bundles already contain RAM. The guide conservatively budgets a separate 128 GB kit, so totals can overstate the incremental purchase cost. Reuse of an owned CPU, RAM or PSU can substantially change the comparison.

## The build selected in the original guide

**TRX40 DESIGNARE + Threadripper 3960X: GBP 800 for motherboard and CPU.**

- Motherboard: GBP 390 paid, as reported by the buyer.
- CPU: GBP 410 paid, as reported by the buyer.
- 24 CPU cores, quad-channel DDR4 and two direct PCIe 4.0 x16 links.
- RAM, PSU, case and cooling are additional unless already owned.

The purchase prices above are buyer-reported, not independently fetched. The cited motherboard listing showed GBP 380; the buyer reported paying GBP 390. This is the original guide's chosen build, not a measured training-performance ranking.

## Power supply budgets

- One 3090: a good 850 W unit; budget 1000 W for a high-power Threadripper system.
- Two stock 3090s: a good 1200-1500 W unit; 1500-1600 W provides more headroom with Threadripper.
- Complete used 850 W PSU budget: about GBP 70-130.
- High-wattage PSU budget: about GBP 200-330; a used Corsair HX1500i was listed at about GBP 197.

These are buying guidelines, not measured electrical loads. Verify the actual PSU condition and the correct PSU/GPU power connectors and cables.

## Memory, lanes and NVLink checks

- X99 DDR3 support is not universal: many X99 boards are DDR4-only. Verify the exact Xeon and motherboard combination. 128 GB can require eight supported DIMM sockets.
- RDIMM and UDIMM are not interchangeable. Some WRX80 boards accept either type; check the exact manual rather than assuming existing consumer DDR4 can be reused.
- The guide budgets about GBP 370-580 for a used 128 GB DDR4 ECC RDIMM 2400-2666 kit; 3200 kits can cost more. Individual cited listings differ.
- For X299 x16/x16, check the exact board and a suitable 44/48-lane CPU, such as the i9-10900X. Cheaper 16/28-lane CPUs cannot be assumed to supply the same wiring.
- X570 does not guarantee CPU-attached x8/x8. Check the exact motherboard manual.
- GPU electrical bandwidth and NVLink bridge fit are separate checks. Verify slot connector positions, card thickness, cooling clearance and case expansion slots. The original DESIGNARE note is conditional; this guide does not supply an independent spacing measurement.
- NVLink does not automatically combine VRAM for every model or application. Whether it helps training requires evidence from the actual workload and software.
- Check for CPU vendor-lock limitations when buying workstation OEM pulls.

## Sources and listing notes

The notes below preserve the original guide's dated observations. Listings can change, expire or sell out.

| Item | Dated observation in the supplied guide | Source |
|---|---|---|
| Gigabyte TRX40 DESIGNARE | Sold 21 Nov 2026 at GBP 380 observed; buyer reported GBP 390 paid | [eBay 117418908135](https://www.ebay.co.uk/itm/117418908135) |
| ASUS PRIME X299-A II + i9-10900X + 32 GB DDR4 | GBP 389.08 asking; Milton Keynes; private seller with limited feedback | [eBay 287716899842](https://www.ebay.co.uk/itm/287716899842) |
| ASUS PRIME X299-A + i9-10900X + 32 GB | GBP 558 asking; Leeds; business seller | [eBay 204804138276](https://www.ebay.co.uk/itm/204804138276) |
| ASUS PRIME X299-A II motherboard | GBP 154.40 asking; Lancing | [eBay 137933286316](https://www.ebay.co.uk/itm/137933286316) |
| ASUS PRIME X299-A II lane rules | Official specifications; x16/x16 depends on CPU lane count | [ASUS specifications](https://www.asus.com/uk/motherboards-components/motherboards/all-series/prime-x299-a-ii/techspec/) |
| Corsair 128 GB DDR4-3200, 4 x 32 GB | GBP 594.23 asking | [eBay 117412258742](https://www.ebay.co.uk/itm/117412258742) |
| 128 GB DDR3 ECC, 8 x 16 GB | GBP 138.24 asking; UK | [eBay 287635528100](https://www.ebay.co.uk/itm/287635528100) |
| 128 GB DDR4 ECC RDIMM 2400, 8 x 16 GB | GBP 369.88; completed September listing | [eBay 168742828427](https://www.ebay.co.uk/itm/168742828427) |
| 128 GB DDR4 ECC RDIMM 2666, 8 x 16 GB | GBP 577.75 asking | [eBay 326632082601](https://www.ebay.co.uk/itm/326632082601) |
| 128 GB DDR4 ECC RDIMM 3200 matched kit | GBP 546.11 completed sale | [eBay 158041102895](https://www.ebay.co.uk/itm/158041102895) |
| Used WRX80 motherboard | GBP 1390 asking; Project-Mac, UK | [eBay 188328222566](https://www.ebay.co.uk/itm/188328222566) |
| X570 boards | Used-market search; only selected boards support CPU x8/x8 | [eBay UK X570](https://www.ebay.co.uk/shop/x570-motherboard?_nkw=x570+motherboard) |
| B550 boards | Used-market search | [eBay UK B550](https://www.ebay.co.uk/shop/b550-motherboard?_nkw=b550+motherboard) |
| Corsair HX1500i 1500 W | GBP 196.92 asking | [eBay 137785872122](https://www.ebay.co.uk/itm/137785872122) |
| Xeon E5-2678 v3 | GBP 35.99 UK listing; out of stock | [eBay 277433013033](https://www.ebay.co.uk/itm/277433013033) |

## Help improve the guide

[Open an issue](https://github.com/turbo-tan/buildAIMachine/issues/new/choose) or submit a pull request. Please include:

1. The section or claim to change, and your proposed correction or alternative.
2. Exact component names and motherboard revision where relevant.
3. A source link and date; distinguish asking prices from completed sales.
4. For performance claims, the workload, software versions, configuration and measured result.
5. For NVLink fit, an exact drawing or measurement plus card and bridge details.

Keep the Markdown and HTML versions aligned when updating figures. Do not turn an unverified compatibility claim or a link-bandwidth ratio into a measured training result.
