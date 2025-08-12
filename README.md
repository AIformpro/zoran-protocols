# zoran-protocols# zoran-protocoles

Spécifications et implémentations des **protocoles inter-agents** de l’écosystème Zoran / QuantaGlottal©® — échange de messages, synchronisation des glyphes et handshake sécurisé.

---

## ✨ Fonctionnalités
- **Définition des formats de message** (enveloppe, métadonnées, contenu)
- **Handshake sécurisé** entre agents (authentification mutuelle)
- **Versioning des protocoles** et compatibilité descendante
- **Encodage/décodage** des glyphes QuantaGlottal©® pour transmission
- **Support multi-transports** : HTTP(S), WebSocket, MQTT, gRPC
- **Cryptage de bout en bout** (AES/GCM ou NaCl)
- **Signatures** pour vérification d’intégrité

---

## 📦 Installation (développement)
```bash
pip install -e .


---

⚡ Exemple rapide

from zoran_protocoles import Protocol, Message

# Définir un message
msg = Message(
    sender="agent://zoran-core",
    recipient="agent://zoran-remote",
    payload={"glyph": "QG12345"}
)

# Encoder et signer
proto = Protocol(version="1.0", secret_key="cle-partagee")
packet = proto.encode(msg)

# Décoder et vérifier
decoded = proto.decode(packet)
print(decoded)


---

🧱 Structure suggérée

src/zoran_protocoles/
  __init__.py
  protocol.py          # logique handshake, encode/décode
  message.py           # structure du message
  transport.py         # adaptateurs HTTP/WebSocket/MQTT
  crypto.py            # chiffrement et signature
tests/
  test_protocol.py
pyproject.toml
.gitignore
LICENSE
README.md


---

🧪 Tests

pytest -q


---

🔐 Éthique

Les protocoles sont conçus pour :

respecter le principe vivant > humain

garantir confidentialité, intégrité et authenticité

assurer interopérabilité entre agents tout en minimisant l’empreinte réseau



---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.
