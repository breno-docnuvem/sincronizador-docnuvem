# Instaladores do Sincronizador

Aqui ficam os **instaladores para Windows** do sincronizador de pasta do DocNuvem. Este repositório contém só o
README e os arquivos de cada versão, na aba **Releases**.

## Baixar

1. Abra a [última versão](../../releases/latest).
2. Em **Assets**, baixe o instalador:

| Arquivo | Para quem |
|---|---|
| `DocNuvem-Sincronizador-Setup.exe` | Instalação com a marca DocNuvem. |
| `Sincronizador-Documentos-Setup.exe` | Versão neutra, para revendedores (white label). |

As duas instalam o mesmo programa. Só mudam os textos, o ícone, o nome do atalho e a pasta padrão do instalador.

## Instalar

1. Execute o instalador **como administrador**.
2. Informe a instância e o token da empresa, a pasta local e o usuário e a senha do DocNuvem. O login é obrigatório.
3. Escolha o disco (o instalador mostra o espaço livre de cada um) e confirme.

Requisitos: Windows 64 bits e acesso de rede à API do DocNuvem. No DocNuvem, **"Ativar Módulo Sincronizador"** deve
estar ligado nas configurações da plataforma.

### Pasta em local de rede

É possível sincronizar para um compartilhamento de rede (`\\servidor\pasta`), mas há regras:

- Use de preferência uma **subpasta vazia**. Tudo o que já estiver na pasta e não estiver no DocNuvem será **enviado**.
- O serviço precisa rodar com uma **conta do Windows com acesso** à pasta (o instalador pede e testa o acesso).
- A **quarentena** fica em uma pasta **local** do computador.

### Instalação em lote (silenciosa)

```
DocNuvem-Sincronizador-Setup.exe /VERYSILENT /SUPPRESSMSGBOXES /Instancia=EMPRESA /Token=XXXX /Usuario=fulano /Senha=segredo [/RaizId=0] [/PastaLocal=C:\DocNuvem]
```

## Aviso do Windows (SmartScreen)

O instalador ainda **não é assinado digitalmente**. O Windows pode exibir "O Windows protegeu seu computador":
clique em **Mais informações → Executar assim mesmo**.

## Suporte

Dúvidas e problemas: _(coloque aqui o contato do suporte)_.
