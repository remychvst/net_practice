*This activity has been created as part of the 42 curriculum by rchavast.*

# NetPractice

## Description

**NetPractice** is a networking exercise from the 42 curriculum whose goal is to make you understand the fundamentals of **computer networking** by solving small, broken network configurations and fixing them so the network works properly.

The project provides a training interface (a simulated network, not connected to any real infrastructure) made of hosts, switches and routers. For each of the 10 levels, a non-functioning network diagram is displayed with one or more objectives (e.g. "host A must be able to communicate with host B"). The task is to edit the unshaded fields — IP addresses, subnet masks, gateways, routes — until the diagram's status turns green and every objective is satisfied.

Through this activity you practice:
- Reading and building a **network diagram**.
- Assigning valid **IP addresses** to interfaces.
- Choosing the correct **subnet mask** for a given network size.
- Configuring the **default gateway** on hosts and routers.
- Understanding how **routers** and **switches** behave differently on a network.
- Reasoning about the **OSI model** layers involved in packet forwarding.

## Instructions

1. Download the archive provided on the activity's page and extract it into a folder of your choice.
2. From that folder, run the provided script:
```bash
   ./run.sh
```
   This launches a local web server and opens the NetPractice interface in your default web browser.

   If `run.sh` does not work (browser security constraints), start the server manually:
```bash
   python3 -m http.server 49242
```
   then open `http://localhost:49242` in your browser (you may use another port if 49242 is busy).

3. On the welcome screen, enter **your 42 login** in the "Training" tab (this lets the moulinette identify your configuration), then click **Start!**.
   You can also use the "Evaluation" tab to generate a random configuration, valid for evaluation purposes.

4. For each of the 10 levels:
   - Read the objective(s) displayed at the top of the page.
   - Fill in the unshaded fields (IP, mask, gateway, routes) so the network functions correctly.
   - Click **Check again** to verify your configuration.
   - Use the logs at the bottom of the page to understand what is wrong (missing gateway, invalid IP, unreachable route, etc.).
   - Once the level is solved, click **Get my config** to export your configuration file.
   - Click **Next level** to move on.

5. Repeat until all 10 levels are completed.

### Submission

- Export **one configuration file per level** using the **Get my config** button (10 files in total).
- Place all 10 exported files **at the root of this Git repository**.
- Double-check that your login was entered in the interface, and that file names match what is expected.

During the defense, you will be asked to solve 3 random levels (from levels 6 to 10) within a limited time, without any external tool other than a simple calculator (e.g. `bc`).

## Resources

Networking concepts studied in this activity:
- **TCP/IP addressing** — how IP addresses identify a host on a network.
- **Subnet masks** — how they define the boundary between network and host portions of an address.
- **Default gateway** — the role of a gateway in routing traffic outside the local subnet.
- **Routers and switches** — differences in how each device forwards traffic.
- **OSI layers** — the layers involved when a packet is forwarded from a host to its destination through routers.

Classic references:
- [Subnetting explained (subnetting.net)](https://www.subnetting.net/)
- [RFC 791 – Internet Protocol](https://www.rfc-editor.org/rfc/rfc791)
- [Cisco Networking Basics – IP Addressing and Subnetting](https://www.cisco.com/)
- [OSI Model overview (Cloudflare Learning)](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

### AI usage

AI (Claude) was used only as a support tool during this activity:
- To clarify theoretical concepts (subnet mask calculation, gateway logic, OSI layer roles) through Q&A, without generating ready-made answers for specific levels.
- To help structure and word this README.md file.

No AI tool was used to solve the levels themselves: every configuration (IP addresses, masks, gateways, routes) was reasoned out and validated manually, and cross-checked with peers before submission.