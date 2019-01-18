---
title: Configurar RDS en Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720957"
---
# <a name="configuring-rds-on-windows-2000"></a>Configurar RDS en Windows 2000


**Se aplica a**: Access 2013, Office 2013

Si tiene dificultades para conseguir que RDS funcione correctamente tras actualizarse a Windows 2000, siga los pasos que se enumeran a continuación para solucionar el problema.

1.  Asegúrese de que el servicio de publicación World Wide Web se está ejecutando primera navegando a https://*servidor* mediante el Explorador de Internet. Si no puede obtener acceso al servidor Web, abra un símbolo del sistema o indicador de comandos y escriba el comando siguiente "NET START W3SVC".

2.  En el menú Inicio, seleccione Ejecutar. Escriba msdfmap.ini y haga clic en Aceptar para abrir el archivo msdfmap.ini en el Bloc de notas. Comprobar la \[CONNECT DEFAULT\] sección y, si el parámetro de acceso se establece en NOACCESS, cámbielo a READONLY.

3.  Uso de la utilidad RegEdit, vaya a "HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" y compruebe que **HandlerRequiredse** establece en 0 y **que DefaultHandler** es "" (Null cadena).
    
    > [!NOTE]
    > [!NOTA] Si realiza algunos cambios en esta sección del Registro, deberá detener y reiniciar el servicio de publicación Web escribiendo los comandos siguientes en un símbolo del sistema: "NET STOP W3SVC" y "NET START W3SVC".

4.  Utilizando RegEdit, desplácese en el registro para "HKEY\_LOCAL\_máquina\\SYSTEM\\CurrentControlSet\\servicios\\W3SVC\\parámetros\\ADCLaunch" y compruebe que haya una clave **llamado RDSServer.Datafactory**. Si no existe, créela.

5.  Uso de administrador de servicios Internet, vaya al sitio Web predeterminado y ver las propiedades de la raíz virtual MSADC. Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio. Si está activada la opción "Acceso denegado", seleccione "Concedido".

Si los cambios no parecen solucionar el problema, intente reiniciar el servidor.

