  
# Guide
## Digital signature for the first time
  ```mermaid
  ---
  tilte: Note
  ---
  flowchart TD
  Login --> Install
  subgraph Login
    direction LR
    Access[Access dichvucong]
    Service[Select service]
    Token[Plug USB token]
    Access --> Service
    Service --> Token
  end
  subgraph Install[Install software]
    direction LR
    Plugin[Install plugin from USB] --> dotNet[Update dot Net framework]
  end
  subgraph Setup[Setup digital signature]
    Upload[Upload signature image] --> Serial[Get serial number]
    Serial --> Save[Save digital signature]
  end
  subgraph Sign
    direction LR
    Click[Click service to sign] --> Pass[Input token password]
  end
  Install --> Setup
  Setup --> Sign
  Sign --> Store([Store USB token])
```

