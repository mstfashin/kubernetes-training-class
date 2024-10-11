kubectl get pods -A

`kubectl` komutu, Kubernetes kümeleri üzerinde çeşitli işlemleri gerçekleştirmek için kullanılır. Pod'ları yönetmek ve listelemek için de sıkça kullanılır. İşte en sık kullanılan `kubectl` komutlarından bazıları ve örnekleri:

### 1. Tüm Pod'ları Listeleme
```bash
kubectl get pods
```
Bu komut, mevcut namespace içindeki tüm Pod'ları listeler.

### 2. Tüm Namespace'lerdeki Pod'ları Listeleme
```bash
kubectl get pods --all-namespaces
```
```bash
kubectl get pods -A
```
Bu komut, tüm namespace'lerdeki Pod'ları listeler.

### 3. Belirli Bir Namespace'teki Pod'ları Listeleme
```bash
kubectl get pods -n <namespace_adi>
```
Örnek:
```bash
kubectl get pods -n kube-system
```

### 4. Pod Detaylarını Görüntüleme
```bash
kubectl describe pod <pod_adi>
```
Bu komut, belirli bir Pod hakkında ayrıntılı bilgi verir.

### 5. Pod'un Detaylarını JSON Formatında Görüntüleme
```bash
kubectl get pod <pod_adi> -o json
```
Pod'un tüm ayrıntılarını JSON formatında görüntüler.

### 6. Pod’un Detaylarını YAML Formatında Görüntüleme
```bash
kubectl get pod <pod_adi> -o yaml
```
Bu komut, Pod'un ayrıntılarını YAML formatında görüntüler.

### 7. Pod'un Loglarını Görüntüleme
```bash
kubectl logs <pod_adi>
```
Pod'un loglarını gösterir. Çoklu konteyner içeren bir Pod için, konteyner adını belirtmek gerekebilir:
```bash
kubectl logs <pod_adi> -c <konteyner_adi>
```

### 8. Pod'ları İzleme (Watch Mode)
Pod'ların durumunu sürekli olarak izlemek için `-w` parametresi kullanılır:
```bash
kubectl get pods -w
```

### 9. Etiketlere Göre Pod'ları Listeleme
```bash
kubectl get pods -l <etiket_anahtari>=<etiket_degeri>
```
Örnek:
```bash
kubectl get pods -l app=myapp
```

### 10. Pod Silme
Belirli bir Pod'u silmek için:
```bash
kubectl delete pod <pod_adi>
```

### 11. Pod YAML’ını Export Etme
Pod'un manifestini dosya olarak dışa aktarmak için:
```bash
kubectl get pod <pod_adi> -o yaml --export > pod.yaml
```

Bu komutlar, Kubernetes üzerinde Pod'ları yönetmek için en çok kullanılan `kubectl` komutlarındandır.

kubectl config get-contexts

![alt](./images/kubectl-config-get-contexts.png)

kubectl get pods -n kube-system

![alt](./images/kubectl-get-pods.png)

kubectl get namespaces

![alt](./images/kubectl-get-namespaces.png)