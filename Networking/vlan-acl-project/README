## English Version

The project aims to design a network divided into VLANs with segmentation for the following departments: HR (VLAN10), IT (VLAN20), Sales (VLAN30) 
and to implement extended ACLs to control communication between VLANs. The entire project was implemented in Cisco Packet Tracer.

### Topology and Devices
- **Switch0:** VLAN10 (HR), VLAN20 (IT)  
- **Switch1:** VLAN30 (Sales)  
- **Router-on-a-Stick:**  
- **PCs (6):**  
  - HR VLAN10 – 2 PCs connected to Switch0  
  - IT VLAN20 – 2 PCs connected to Switch0  
  - Sales VLAN30 – 2 PCs connected to Switch1  

### Features
- VLAN configuration on switches
- Trunk links between switches and router
- Router-on-a-Stick for inter-VLAN routing
- Extended ACLs blocking:
  - Sales -> HR
  - HR -> Sales

### Implementation Steps
1. **VLAN Creation:** Created VLAN10 (HR), VLAN20 (IT), VLAN30 (Sales) on switches.
2. **Assign Ports to VLANs:** Connected PCs to switches and assigned their ports to the appropriate VLAN.
3. **Configure Trunk Links:** Set trunk ports between switches and the router to carry multiple VLANs.
4. **Router-on-a-Stick Setup:** Created subinterfaces on the router for each VLAN with appropriate IP addresses.
5. **Configure Extended ACLs:** 
   - ACL 100: Blocks Sales -> HR
   - ACL 101: Blocks HR -> Sales
6. **Apply ACLs to Subinterfaces:** Applied ACLs in the correct direction on router subinterfaces.
7. **Testing Connectivity:** 
   - Verified intra-VLAN communication (PCs within same VLAN)
   - Verified inter-VLAN communication before ACLs
   - Verified access control after ACLs

### Verification / Test Results
- **Intra-VLAN connectivity:** PCs within the same VLAN can ping each other successfully.
- **Inter-VLAN connectivity before ACLs:** All VLANs can communicate freely.
- **Inter-VLAN connectivity after ACLs:** 
  - HR <-> IT – allowed
  - Sales <-> IT – allowed
  - Sales -> HR – blocked
  - HR -> Sales – blocked

### Configuration Files
- `router-config.txt` – router configuration
- `switch0-config.txt` – Switch0 configuration
- `switch1-config.txt` – Switch1 configuration

### In addition
- `./assets/topology/topology.png` – network topology diagram
- `./assets/screenshots/before-acl/.. - ping screenshots taken before setting acl's 
- `./assets/screenshots/with-acl/.. - ping screenshots taken after setting acl's 
- `./assets/subnets.txt` - ip addressing 
- `./assets/screenshots/acl_lists_router.png` - a list of acl's on a router
---

## Wersja Polska

Projekt ma na celu zaprojektowanie sieci podzielonej na VLAN'y z segmentacją działów: HR (VLAN10), IT (VLAN20) i Sales (VLAN30) oraz 
zastosowanie rozszerzonych ACL w celu kontrolowania komunikacji między VLAN-ami. Całość została zrealizowana w Cisco Packet Tracer.

### Topologia i urządzenia
- **Switch0:** VLAN10 (HR), VLAN20 (IT)  
- **Switch1:** VLAN30 (Sales)  
- **Router na patyku**
- **PC (6):**  
  - HR VLAN10 – 2 PC podłączone do Switch0  
  - IT VLAN20 – 2 PC podłączone do Switch0  
  - Sales VLAN30 – 2 PC podłączone do Switch1  

### Funkcjonalności
- Konfiguracja VLAN-ów na switchach
- Trunki między switchami i routerem
- Router-on-a-Stick dla routingu między VLAN-ami
- Rozszerzone ACL blokujące:
  - Sales -> HR
  - HR -> Sales

### Kroki realizacji
1. **Tworzenie VLAN-ów:** Utworzono VLAN10 (HR), VLAN20 (IT), VLAN30 (Sales) na odpowiednich switchach.
2. **Przypisanie portów do VLAN-ów:** Podłączono PC do switchy i przypisano ich porty do właściwych VLAN-ów.
3. **Konfiguracja trunków:** Skonfigurowano porty na tryb trunk między switchami a routerem, aby przesyłały ruch dla wielu VLAN-ów.
4. **"Router na patyku"** Utworzono subinterfejsy na routerze dla każdego VLAN z odpowiednimi adresami IP.
5. **Konfiguracja rozszerzonych ACL:** 
   - ACL 100: blokuje Sales -> HR
   - ACL 101: blokuje HR -> Sales
6. **Przypisanie ACL do subinterfejsów:** Zastosowano ACL na subinterfejsach routera.
7. **Testowanie połączeń:** 
   - Sprawdzenie komunikacji w obrębie VLAN-ów (PC w tym samym VLAN)
   - Sprawdzenie komunikacji między VLAN-ami przed włączeniem ACL
   - Weryfikacja widoczności po włączeniu ACL

### Weryfikacja / Wyniki testów
- **Komunikacja w obrębie VLAN:** PC w tym samym VLAN mogą się pingować poprawnie.
- **Komunikacja między VLAN-ami przed włączeniem ACL:** wszystkie VLAN-y mogą komunikować się swobodnie.
- **Komunikacja między VLAN-ami po włączeniu ACL:** 
  - HR <-> IT – dozwolone
  - Sales <-> IT – dozwolone
  - Sales -> HR – zablokowane
  - HR -> Sales – zablokowane

### Pliki konfiguracyjne
- `router-config.txt` – konfiguracja routera
- `switch0-config.txt` – konfiguracja switcha 0
- `switch1-config.txt` – konfiguracja switcha 1

### Dodatki
- `./assets/topology/topology.png` – topologia w formie graficznej
- `./assets/screenshots/before-acl/.. - screeny polecenia "ping" przed wprowadzeniem acl 
- `./assets/screenshots/with-acl/.. - screeny polecenia "ping" po wprowadzeniu acl
- `./assets/subnets.txt` - adresy ip / podsieci
- `./assets/screenshots/acl_lists_router.png` - lista aktualnych acl na routerze 
