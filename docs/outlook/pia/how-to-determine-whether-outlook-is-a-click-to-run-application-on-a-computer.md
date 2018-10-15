---
title: Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c155fed72a314c5c260ed2fe574474afd45c44c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406655"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a>Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo

Hacer clic y ejecutar es una entrega del software y el mecanismo de actualización disponible para Office 2010 y versiones posteriores. Los productos que se envíen mediante Hacer clic y ejecutar se ejecutan en un entorno virtual de aplicación del sistema operativo local. Esto significa que tienen copias privadas de sus archivos y configuración, y que los cambios que realizan se capturan en el entorno virtual.

Hacer clic y ejecutar es rápido, los usuarios pueden iniciar la ejecución de una aplicación en poco tiempo sin tener que esperar que el producto completo finalice la instalación. Las actualizaciones se ejecutan automáticamente en el fondo, sin que un usuario tenga que quitar primero una instalación o instalar actualizaciones de forma manual. Los productos de Hacer clic y ejecutar se virtualizan y no entran en conflicto con otro software instalado. Pero, como un producto entregado por Hacer clic y ejecutar tiene copias privadas de todos sus archivos y del registro, un desarrollador de complementos no puede determinar la existencia del producto de la misma manera que un producto que se instaló en el disco duro del equipo cliente. Desde Outlook 2010, los desarrolladores de complementos deben comprobar si Outlook está instalado y si se ha entregado Outlook como un producto de Hacer clic y ejecutar.


> [!NOTE]
> En el entorno de aplicación virtual de Hacer clic y ejecutar solo se admite Office 2013 de 32 bits, incluso si el equipo cliente ejecuta un sistema operativo de 64 bits.



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a>Para comprobar si Outlook 2013 se entregó mediante Hacer clic y ejecutar en un equipo cliente

- Comprobar si la clave VirtualOutlook existe en la siguiente ubicación del registro de Windows:
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  La clave VirtualOutlook es un valor REG\_SZ que contiene la etiqueta de referencia cultural del idioma del producto instalado, como "en-us".

## <a name="see-also"></a>Vea también

- [Administración de complementos](add-in-administration.md)

