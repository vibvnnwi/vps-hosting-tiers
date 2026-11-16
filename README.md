# Linux VPS hosting: which tier do you actually need, managed or root, and what does renewal really cost? (Plan table, overage fees, and the $300 credit)

Three things decide whether a Linux VPS is good value: the price after the intro term ends, whether you get root or a control panel, and how overage gets billed. Miss any of them and a $6 server can cost more than a $12 one.

The gap is easy to see in current listings. Hostinger shows KVM 1 at $6.49/mo, which means paying $155.76 today for 24 months and renewing at $11.99/mo. Contabo lists Cloud VPS 4 at €5.50/mo but charges €4.40/mo for the first 24 months. Vultr's shared tiers run from $5/mo for 1 vCPU / 1 GB / 25 GB SSD up to $6/mo for NVMe storage, and new accounts can claim a $300 credit with the code published on Vultr's coupons page.

Below: a full tier table, the arithmetic on first-term versus renewal pricing, the root-access difference between managed and self-managed, and the fees that only appear in the terms.

> **Most readers:** a 1 vCPU / 1–2 GB NVMe instance at $6–$12/mo handles a low-traffic site, a small API, or a Docker side project. Move to 2 vCPU / 4 GB ($24) when you add a database or a second app. If you're evaluating infrastructure rather than running one site, the $300 new-account credit lets you run the $48–$96 tiers for a test window instead of guessing from specs. 👉 [See Vultr's current tiers and the $300 credit terms](https://bit.ly/VuLtr)

## What $5 to $96 a month buys on Vultr

The line-up splits into three shared-CPU families. Regular Cloud Compute runs on previous-generation Intel with standard SSD and is the cheapest entry point. High Performance moves to current AMD EPYC or Intel Xeon with NVMe. High Frequency uses 3 GHz+ Xeon chips with NVMe, which matters for single-thread-bound work like PHP or a small Postgres instance.

| Plan (shared CPU) | vCPU | RAM | Storage | Price / mo |  |
| --- | --- | --- | --- | --- | --- |
| Regular 1 GB | 1 | 1 GB | 25 GB SSD | $5 | [See plan](https://bit.ly/VuLtr) |
| Regular 2 GB | 1 | 2 GB | 55 GB SSD | $10 | [See plan](https://bit.ly/VuLtr) |
| Regular 2 vCPU / 2 GB | 2 | 2 GB | 65 GB SSD | $15 | [See plan](https://bit.ly/VuLtr) |
| Regular 4 GB | 2 | 4 GB | 80 GB SSD | $20 | [See plan](https://bit.ly/VuLtr) |
| Regular 8 GB | 4 | 8 GB | 160 GB SSD | $40 | [See plan](https://bit.ly/VuLtr) |
| High Performance 1 GB | 1 | 1 GB | 25 GB NVMe | $6 | [See plan](https://bit.ly/VuLtr) |
| High Performance 2 GB | 1 | 2 GB | 50 GB NVMe | $12 | [See plan](https://bit.ly/VuLtr) |
| High Performance 4 GB | 2 | 4 GB | 100 GB NVMe | $24 | [See plan](https://bit.ly/VuLtr) |
| High Performance 8 GB | 4 | 8 GB | 180 GB NVMe | $48 | [See plan](https://bit.ly/VuLtr) |
| High Performance 16 GB | 8 | 16 GB | 350 GB NVMe | $96 | [See plan](https://bit.ly/VuLtr) |
| High Frequency 1 GB | 1 | 1 GB | 32 GB NVMe | $6 | [See plan](https://bit.ly/VuLtr) |
| High Frequency 2 GB | 1 | 2 GB | 64 GB NVMe | $12 | [See plan](https://bit.ly/VuLtr) |
| High Frequency 4 GB | 2 | 4 GB | 128 GB NVMe | $24 | [See plan](https://bit.ly/VuLtr) |
| High Frequency 8 GB | 3 | 8 GB | 256 GB NVMe | $48 | [See plan](https://bit.ly/VuLtr) |
| High Frequency 16 GB | 4 | 16 GB | 384 GB NVMe | $96 | [See plan](https://bit.ly/VuLtr) |

Above those sit the dedicated-CPU tiers, where the core is yours alone rather than shared with other tenants on the host:

| Plan (dedicated CPU) | vCPU | RAM | Storage | Price / mo |  |
| --- | --- | --- | --- | --- | --- |
| CPU-Optimized | 1 | 2 GB | 25 GB NVMe | $28 | [See plan](https://bit.ly/VuLtr) |
| General Purpose | 1 | 4 GB | 30 GB NVMe | $30 | [See plan](https://bit.ly/VuLtr) |
| Memory-Optimized | 1 | 8 GB | 50 GB NVMe | $40 | [See plan](https://bit.ly/VuLtr) |

Two notes on the numbers. These are the listed monthly rates for these tiers as of late 2026, and Vultr rotates plan line-ups, so confirm the figure on the order page before you budget. Transfer allowances scale with the tier, from roughly 1 TB on the smallest instance to several TB on the larger ones, and the overage rate is quoted at checkout rather than in the plan name.

## The same money elsewhere, for benchmark purposes

Worth knowing what the competition charges for comparable specs, because two of these look cheaper per gigabyte until you read the term.

| Provider and plan | vCPU | RAM | Storage | Price and term |
| --- | --- | --- | --- | --- |
| Hostinger KVM 1 | 1 | 4 GB | 50 GB NVMe | $6.49/mo on a 24-month prepay ($155.76 today), renews at $11.99/mo |
| Hostinger KVM 4 | 4 | 16 GB | 200 GB NVMe | $12.99/mo on a 24-month prepay ($311.76 today), renews at $28.99/mo |
| Contabo Cloud VPS 4 | 4 | 8 GB | 100 GB SSD | €5.50/mo list, €4.40/mo for the first 24 months |
| Contabo Cloud VPS 6 | 6 | 12 GB | 200 GB SSD or 100 GB NVMe | €7.50/mo list, €6.00/mo for the first 24 months |
| Liquid Web Compute | 1 | 2 GB | 60 GB | $11/mo or $0.015/hr, fully managed |

Hostinger wins on raw specs per dollar if you'll commit 24 months and pay up front. Contabo wins on specs per euro, with the caveat that Cloud VPS 4 ships a 200 Mbit/s port and Cloud VPS 6 a 300 Mbit/s port, so "unlimited traffic" comes with a throughput ceiling. Vultr's $6 tier is a $6 tier, with no four-figure prepay and no first-term discount structure attached to it, which is the difference between a tier you can try and a contract you have to justify.

## First-term price versus renewal price

This is where the cheap headline numbers fall apart. Hostinger's KVM 1 is $6.49/mo for the first 24 months and $11.99/mo after that, a 1.85× jump. KVM 4 goes from $12.99 to $28.99, which is 2.23×. KVM 8 goes from $25.99 to $49.99, 1.92×.

Run the four-year total on KVM 1: $155.76 upfront, then $287.76 for the next 24 months at the renewal rate, or $443.52 in total. That works out to about $9.24/mo blended, not $6.49. The $6.49 figure is real, but it's a two-year average that requires paying the whole term on day one. Budget on the renewal rate and treat the discount as a rebate you get for committing early.

Contabo's numbers use a different qualifier: "for the first 24 months," against a €5.50 list price on Cloud VPS 4. The renewal price isn't published in that listing, and Contabo's terms say the minimum renewal period matches the initial term and that postpaid cancellations need four weeks' notice. If you take a 24-month promotional term, read the renewal term you're agreeing to alongside it.

Liquid Web adds a third wrinkle: its promotions apply to new accounts only and don't carry over to upgrades of existing servers. So the discounted price you sign up at disappears the moment you resize.

## Managed, self-managed, and who actually gets root

Root access is the clearest dividing line, and it doesn't track price.

hosting.com sells managed cPanel VPS and states plainly that root isn't included, by design. You get CloudLinux isolation, LiteSpeed, daily backups and a 99.99% uptime guarantee, and if you want direct OS control they'll point you to their unmanaged products. Extra cPanel accounts are billed at pass-through cost, timed to cPanel's monthly invoicing around the 15th.

Liquid Web sells "fully managed" and still hands you root-level access, plus a 100% uptime guarantee. One detail to watch on their page: the header says "starting at $17/mo" while the Compute table's lowest row is 1 vCPU / 2 GB / 60 GB at $11/mo. Budget from the row you'd actually order.

Hostinger is explicitly self-managed with full root, backed by tutorials and an AI assistant rather than hands-on administration. Contabo describes its offering as "not a managed Linux VPS" and expects you to run multiple virtual servers yourself.

If you want root and don't mind patching, the instance-based providers are the natural fit. If you never want to see a terminal, buy managed cPanel and accept that root isn't part of the package. 👉 [Start a Vultr account with the $300 credit applied](https://bit.ly/VuLtr)

## Line items that never make the headline price

The extras are small individually and add up over a year.

Additional IPv4 addresses cost $3.65/mo each at Atlantic.Net ($0.005431/hr), and outbound transfer beyond the allowance is $0.02/GB, with inbound unmetered. Two extra IPs on a $10 server is a 73% price increase nobody mentions in a review.

Bandwidth "unlimited" usually means unmetered volume at a capped port speed, as with Contabo's 200–800 Mbit/s ports across Cloud VPS 4 through 12. If your workload is bursty rather than sustained, port speed decides your user experience more than the traffic quota does.

Control panel licences are the other recurring line. A single cPanel account is typically bundled into a managed plan, but additional accounts get charged at the provider's pass-through rate, and the billing date follows the panel vendor's cycle rather than your hosting renewal.

## The $300 credit: what it covers, and what it won't combine with

Vultr's official coupons page lists a $300 free credit code (FLY300VULTR) alongside a $200 code, a $250 code, and a deposit-match code that doubles your first deposit up to $100. The terms printed there are consistent across all of them: promotional credit applies to select products only, cannot be combined with any other offers, and is for new customers only.

That last clause is the practical one. You pick either the $300 credit or the deposit match, not both. The credit is also a product balance rather than cash, so it may not cover every add-on on the platform, and the coupon page doesn't publish an expiry window. Check the balance and its expiry in Billing after signup, before you plan a month-long test around it.

Used sensibly, the credit answers the question this article can't answer from a spec sheet: whether a $48 High Performance 8 GB instance is actually faster for your workload than a $12 one. Deploy both, run your own benchmark, keep the smaller one.

## Quick answers

**Is 1 GB of RAM enough for a Linux VPS?** For Nginx plus a static site, a small Node or Python service, or a WireGuard endpoint, yes. Add a MySQL database and a PHP stack and 2 GB is the realistic floor, which is why the $12 tier is the most common starting point rather than the $5 one.

**Do I need a control panel?** Only if someone who won't touch SSH needs to manage sites, mail or DNS. A panel adds licence cost and a second thing to patch. For a single app you deploy from Git, skip it.

**What happens when I exceed the bandwidth allowance?** Providers bill per GB beyond the allowance or throttle the port. Rates live on the order page, not the plan card, so pull the number before you pick a tier size.

**Can I run Windows instead?** The tiers here are sold with Linux images; Windows licensing is a separate question on most platforms. Pick a provider that prices it explicitly if that's your requirement.

## How to decide in one minute

Running one low-traffic site or a side project: take the $6 High Performance or High Frequency 1 GB tier. Two vCPU / 4 GB at $24 once a database, a queue worker, or a second app enters the picture.

You want root, custom kernels, Docker, or a specific distro: stay with instance-based hosting and budget your own maintenance time. You want cPanel, white-labelled client logins and someone else patching CloudLinux: buy managed, and expect to give up root.

You're still choosing between architectures: spend the $300 credit on the expensive tiers first, measure, then commit to the $6–$12 tier you actually need.

Two things to confirm before you pay anywhere: the renewal rate and term length in writing, and the per-unit price of anything you'll add later (extra IPs, extra cPanel accounts, egress). 👉 [Check Vultr's plan list and claim the new-account credit](https://bit.ly/VuLtr)
