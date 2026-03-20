# Wazuh SIEM LAB – Środowisko Testowe

## Opis projektu
Projekt zakłada wdrożenie systemu SIEM (Security Information and Event Management) 
opartego na platformie Wazuh w środowisku wirtualnych maszyn z systemem Linux. 
Celem projektu jest monitorowanie bezpieczeństwa systemu oraz wykrywanie zagrożeń.

## Architektura
- Maszyna 1 – Wazuh Server: Ubuntu Server 22.04 LTS, Wazuh Manager + Indexer + Dashboard v4.14.4
- Maszyna 2 – Wazuh Agent: Ubuntu Desktop 22.04 LTS, Wazuh Agent v4.14.4
- Sieć: VirtualBox Host-Only (192.168.56.0/24) + NAT

## Technologie
- Wazuh 4.14.4
- Ubuntu 22.04 LTS
- VirtualBox
- OpenSearch
- auditd

## Zrealizowane funkcjonalności

### 1. Monitorowanie aktywności użytkowników
- Monitorowanie logowań SSH i nieudanych prób logowania
- Wykrywanie użycia sudo i eskalacji uprawnień
- Rejestrowanie wykonywanych poleceń przez auditd
- Monitorowanie zmian w plikach systemowych (FIM)

### 2. Wykrywanie podatności CVE
- Integracja z bazą NVD (National Vulnerability Database)
- Automatyczne skanowanie zainstalowanych pakietów
- Wykrywanie podatności z podziałem na poziomy: Critical, High, Medium, Low
- Powiadomienia o nowych CVE

### 3. File Integrity Monitoring (FIM)
- Monitorowanie katalogów /etc, /bin, /sbin, /usr/bin w trybie realtime
- Wykrywanie dodanych, zmodyfikowanych i usuniętych plików
- Rejestrowanie zmian zawartości plików

### 4. Security Configuration Assessment (SCA)
- Skanowanie konfiguracji systemu zgodnie z CIS Benchmark dla Ubuntu 22.04
- Wynik: 46% (po podstawowej konfiguracji systemu)
- Wykrywanie błędnych konfiguracji i rekomendacje naprawcze

## Wyniki
| Funkcja | Status |
|---------|--------|
| Monitorowanie użytkowników | ✅ Działa |
| Wykrywanie CVE | ✅ Działa |
| File Integrity Monitoring | ✅ Działa |
| Security Configuration Assessment | ✅ Działa |

## Screenshots
*(folder /screenshots)*
