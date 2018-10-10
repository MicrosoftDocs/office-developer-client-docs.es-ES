---
title: Configurar RDS en Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1f3227e7ae60d1b656b1a7e82b4a2d41bc36844
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485643"
---
# <a name="configuring-rds-on-windows-2000"></a>Configurar RDS en Windows 2000


**Se aplica a**: Access 2013 | Office 2013

Si tiene dificultades para conseguir que RDS funcione correctamente tras actualizarse a Windows 2000, siga los pasos que se enumeran a continuación para solucionar el problema.

1.  Asegúrese de que el servicio de publicación World Wide Web se está ejecutando primera navegando a https://*servidor* mediante el Explorador de Internet. Si no puede obtener acceso al servidor Web, abra un símbolo del sistema o indicador de comandos y escriba el comando siguiente "NET START W3SVC".

2.  En el menú Inicio, seleccione Ejecutar. Escriba msdfmap.ini y haga clic en Aceptar para abrir el archivo msdfmap.ini en el Bloc de notas. Comprobar la \[CONNECT DEFAULT\] sección y, si el parámetro de acceso se establece en NOACCESS, cámbielo a READONLY.

3.  Uso de la utilidad RegEdit, vaya a "HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" y compruebe que **HandlerRequiredse** establece en 0 y **que DefaultHandler** es "" (Null cadena).
    

    > [!NOTE]
    > <P>[!NOTA] Si realiza algunos cambios en esta sección del Registro, deberá detener y reiniciar el servicio de publicación Web escribiendo los comandos siguientes en un símbolo del sistema: "NET STOP W3SVC" y "NET START W3SVC".</P>



4.  Utilizando RegEdit, desplácese en el registro para "HKEY\_LOCAL\_máquina\\SYSTEM\\CurrentControlSet\\servicios\\W3SVC\\parámetros\\ADCLaunch" y compruebe que haya una clave **llamado RDSServer.Datafactory**. Si no existe, créela.

5.  Mediante Internet Services Manager, vaya el sitio Web predeterminado y vea las propiedades de la raíz virtual MSADC. Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio. Si está activada la opción "Acceso denegado", seleccione "Concedido".

Si los cambios no parecen solucionar el problema, intente reiniciar el servidor.

