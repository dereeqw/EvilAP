# EvilAP v1.9.0-beta

Rogue Access Point + Captive Portal + DNS Spoof + Transparent Proxy

EvilAP crea un Access Point falso con portal cautivo, spoofing DNS y proxy HTTP transparente. Permite interceptar tráfico HTTP, registrar consultas DNS, capturar credenciales y controlar el acceso a Internet por cliente.

---

## 🔥 Características

- Rogue AP con hostapd
- Servidor DHCP/DNS con dnsmasq
- DNS Spoof (wildcard, selectivo o desactivado)
- Proxy HTTP transparente
- Intercepción HTTPS con certificado autofirmado
- Portal cautivo integrado o servidor externo
- Captura automática de credenciales
- Control por cliente (allow, revoke, kick)
- Sniffer TLS SNI
- Soporte NAT opcional
- Interfaz CLI interactiva

---

## 📦 Requisitos

Sistema Linux (Kali recomendado)

Instalar dependencias:

apt install hostapd dnsmasq iw iptables openssl tcpdump arping
pip install prompt_toolkit

Debe ejecutarse como root.

---

## 🚀 Instalación

git clone https://github.com/dereeqw/EvilAP.git
cd EvilAP
chmod +x evilAP.py

---

## ⚙️ Uso

sudo python3 evilAP.py

El asistente interactivo solicitará:

- Interfaz WiFi
- SSID
- WPA2 opcional
- Canal
- Gateway
- NAT opcional
- Modo portal (DNS o Popup)
- DNS Spoof
- Portal integrado o servidor externo

---

## 🌐 Servidor Externo (Opcional)

sudo python3 evilAP.py --portal-server 10.0.0.1:5000

---

## 🔐 Gestión de Clientes

allow <ip>
revoke <ip>
kick <ip>
clients
creds

---

## 📁 Archivos Generados

- credentials.txt
- credentials.json
- traffic.json
- /tmp/evil_ap/

---

## 🔄 DNS Spoof

- Wildcard → Todos los dominios → Gateway
- Selectivo → Solo dominios definidos
- Off → Solo logging

---

## 🛑 Advertencia Legal

Solo para:
- Laboratorios
- Auditorías autorizadas
- Investigación en seguridad
- Entornos controlados

El uso en redes sin autorización es ilegal.

---

## 📜 Licencia

Research / Educational Use Only

Permitido:
- Uso personal
- Investigación interna
- Laboratorio

Prohibido:
- Uso comercial
- Uso en redes sin autorización
---
