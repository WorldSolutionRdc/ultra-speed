# Proxy Nginx pour VPS 31.59.120.101

Service Cloud Run agissant comme proxy TCP vers le VPS `world-speed-drc`.

## Configuration
- **VPS cible :** `31.59.120.101:443`
- **Port du proxy :** `8080`
- **Région Cloud Run :** `europe-west2` (Londres)
- **Compte de service :** `unlimited-france`

## Déploiement
```bash
gcloud run deploy speed-faster \
  --source . \
  --region europe-west2 \
  --allow-unauthenticated \
  --port 8080 \
  --memory 256Mi \
  --timeout 3600 \
  --service-account unlimited-france@project-35c16924-9301-4126-9f5.iam.gserviceaccount.com
