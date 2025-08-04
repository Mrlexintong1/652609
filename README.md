Optimización y documentación técnica de red WiFi banda 5 GHz con enfoque Cisco.
# Optimización Técnica de Red WiFi - Banda 5 GHz

Este documento describe los cambios implementados en la infraestructura de red inalámbrica de un entorno empresarial, enfocado en mejorar la estabilidad, el rendimiento y la calidad de servicio en una red con múltiples puntos de acceso y más de 70 dispositivos conectados.

## ⚙️ Contexto Inicial

Se presentaban los siguientes problemas:
- Latencia elevada y fluctuante
- Interferencias constantes
- Baja velocidad en ciertos puntos
- Conexiones inestables y caídas
- Uso ineficiente del espectro inalámbrico

---

## ✅ Cambios Técnicos Aplicados

### 1. Desactivación de la banda de 2.4 GHz
- Alta interferencia por saturación de canales (solo 3 no traslapados).
- Se eliminó el tráfico innecesario de dispositivos IoT y legacy.
- Beneficio: Reducción de ruido e interferencias.

### 2. Fijación manual de canales en 5 GHz (sin DFS)
- Se eliminaron canales DFS para evitar interrupciones por radar.
- Se usaron canales UNII-1 y UNII-3: 36, 40, 44, 48, 149, 153, 157, 161.
- Beneficio: Mayor estabilidad de canal y menor latencia.

### 3. Reducción de ancho de canal: 80 MHz → 40 MHz
- Se priorizó la estabilidad sobre el throughput teórico.
- Mejora en coexistencia entre APs y reducción de colisiones.
- Beneficio: Mejora en calidad de señal y menos solapamientos.

### 4. Segmentación de canales por AP
- Se asignaron canales fijos y únicos por AP.
- Se evitó el uso de canales adyacentes en celdas cercanas.
- Beneficio: Reducción de interferencia co-canal y mejora en roaming.

### 5. Ajuste de potencia de transmisión
- Se calibró la potencia para evitar sobrecobertura.
- Se optimizó cobertura por celda según la disposición física del sitio.
- Beneficio: Red balanceada y mejor control de roaming.

### 6. Desactivación de funciones automáticas
- Se desactivaron:
  - Auto Channel
  - Auto Power
  - DFS Dynamic Detection
- Beneficio: Estabilidad y control total por parte del administrador.

---

## 📈 Resultados Obtenidos

| Métrica                  | Antes       | Después     |
|--------------------------|-------------|-------------|
| Latencia promedio        | > 80 ms     | < 20 ms     |
| Pérdida de paquetes      | Hasta 15%   | 0 – 2%      |
| Roaming entre APs        | Inestable   | Fluido      |
| Throughput promedio      | Variable    | Constante   |
| Interferencias internas  | Alta        | Muy baja    |
| Reclamos de usuarios     | Frecuentes  | Casi nulos  |

---

##  Conclusión Técnica

La red fue migrada completamente a 5 GHz, con control de canales, ancho de banda reducido, y parámetros fijos alineados con las mejores prácticas de Cisco. Se priorizó la eficiencia espectral, estabilidad de conexión y una experiencia de usuario sólida en entornos de alta densidad.

---

**Autor:** Carlos Tlali Rosales  
**Rol:** Administrador de red / Especialista en IT / Ciberseguridad  
**Fecha de implementación:** 2025
