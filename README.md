# watch-teacher
BTU Bilgisayar Mühendisliği labları için hoca izleme dosyaları


Kullandığınız cihazın etiketine bakın ve lab numarasını not alın. Örn; etikette lab2pc19 görüyorsanız lab2 klasörüne gidin.

Başlattığınız işletim sistemine göre uygun klasöre gidin.

Linux için "IZLE" dosyasını masaüstüne atın ve özelliklerden çalıştırma izni verin. Daha sonra çift tıklayıp "Uç birimde çalıştır" dediğinizde hoca bilgisayarını izlemeye başlayabilirsiniz.

Windows için "viewer.exe" ve "vncopt.vnc" dosyalarını Bilmuh/VNC klasörünün içerisine kopyalayın. Varsa, diğer dosyaların üzerine yazın. "IZLE.bat" dosyasını ise masaüstüne yerleştirin.


---

Win10 SSH Aktivasyonu
```powershell
# List of services to manage
$services = @("sshd", "ssh-agent")

foreach ($service in $services) {
    # Start the service
    Write-Host "Starting the $service service..."
    Start-Service $service

    # Set the service to start automatically
    Write-Host "Setting the $service service to start automatically..."
    Set-Service -Name $service -StartupType 'Automatic'
}

Write-Host "Both 'OpenSSH Authentication Agent' and 'OpenSSH SSH Server' services have been set to start automatically and have been started."
```
