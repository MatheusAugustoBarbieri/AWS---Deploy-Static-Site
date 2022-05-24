DEPLOY FRONT END - static

1. Build project
2. Amazon S3
3. Criar Bucket(repositorio de arquivos)---"nome do bucket tem que ser exatamente igual o da url do site"
4. Ter um dominio
5. Assim que criado o bucket, arraste os arquivos front para dentro dele
6. Next next e upload
7. Properties - static website hosting
8. Selecione - Use this bucket to host a website (index.html nas duas opções)
9. Criar nova entrada (Pegue o endereço gerado e altere aponte o DNS com o nome que deseja pra ele)

Criar Certificado

1. Certicate Manager
2. Provision certificates - Get Started
3. Request a certificate
4. Adicionar o dominio(ou dominios) que deseja adicionar o certificado
5. DNS validation
6. Confirm and request
7. Adicione o Name e o Value gerados no seu DNS

Criar CDN

1. CloudFront
2. Create Distribution
3. Web - Get Started
4. configs{
   Domain: "nome do seu dominio criado pela amazom",
   Viewer Protocol Policy: "Redirect HTTP to HTTPS",
   Alternate Domain Names (CNAMEs): "Nome alternativo que voce apontou para o dominio criado pela amazom",
   Custom SSL Certificate: "Certificado criado por você",
   Default Root Object: index.html
   }
5. Create Distribution
6. Pegar Domain Gerado no CloudFront
7. No DNS criar nova entrada e colar o Domain gerado do CloudFront
