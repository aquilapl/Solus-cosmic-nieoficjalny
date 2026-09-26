# COSMIC Desktop na Solus

## Opcja 1 — z katalogu

```bash
cd ~/Pobrane/cosmic_paczki/

for pkg in xdg-desktop-portal-cosmic cosmic-applets cosmic-panel cosmic-files \
           cosmic-applibrary cosmic-comp cosmic-osd cosmic-randr cosmic-settings \
           cosmic-workspaces cosmic-wallpapers cosmic-greeter cosmic-idle cosmic-bg \
           cosmic-sound-theme cosmic-settings-daemon cosmic-notifications cosmic-session \
           cosmic-icons cosmic-edit cosmic-initial-setup cosmic-screenshot cosmic-term \
           cosmic-monitor cosmic-store cosmic-player cosmic-launcher cosmic-viewer; do
    sudo eopkg it "$pkg"*.eopkg
done

sudo eopkg it cosmic-desktop*.eopkg
```

Zawiesza się na jakimś pakiecie:
```bash
sudo eopkg check
sudo eopkg it -D nazwa_pakietu*.eopkg
```

## Opcja 2 — lokalne repo

```bash
cd ~/Pobrane/cosmic_paczki/
sudo eopkg index --skip-signing .
sudo eopkg ar cosmic-repo ~/Pobrane/cosmic_paczki/eopkg-index.xml.xz
sudo eopkg it cosmic-desktop
```

Aktualizacja repo po dodaniu nowych paczek do katalogu:
```bash
sudo eopkg index --skip-signing .
sudo eopkg ur
```

## Licencje

Poszczególne pakiety COSMIC pochodzą z github.com/pop-os i zachowują licencje nadane przez System76 (GPL-3.0 dla aplikacji, MPL-2.0 dla części bibliotek, CC-BY-SA-4.0 dla ikon).
