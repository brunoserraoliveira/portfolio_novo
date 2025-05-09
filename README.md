# Portfólio Pessoal na AWS

Meu portfólio está hospedado na AWS utilizando os seguintes serviços:

- **Amazon S3**: armazena os arquivos estáticos do portfólio (HTML, CSS, JS).
- **Amazon CloudFront**: entrega o conteúdo do S3 de forma rápida e segura por meio de uma CDN.
- **Amazon Route 53**: gerencia o DNS do domínio personalizado `www.bruno-oliveira-portfolio.com.br`.
- **AWS Certificate Manager (ACM)**: fornece o certificado SSL para acesso seguro (HTTPS).

## Fluxo de Funcionamento

1. Criei um **script Shell de deploy automatizado** que envia os arquivos para o bucket S3:
   - O comando executa o upload dos arquivos locais para o S3.
   - Garante que os arquivos estejam públicos e com os metadados corretos.
   - Após o upload, o CloudFront automaticamente entrega a nova versão do site.
2. O **CloudFront** distribui o conteúdo com baixa latência e HTTPS.
3. O **Route 53** aponta o domínio `www.bruno-oliveira-portfolio.com.br` para a distribuição do CloudFront.

A URL final do portfólio é:  
👉 **[https://www.bruno-oliveira-portfolio.com.br](https://www.bruno-oliveira-portfolio.com.br)**

---
