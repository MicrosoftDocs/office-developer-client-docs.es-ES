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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296020"
---
# <a name="configuring-rds-on-windows-2000"></a>Configuración de RDS en Windows 2000


**Se aplica a:** Access 2013, Office 2013

Si tiene dificultades para conseguir que RDS funcione correctamente tras actualizarse a Windows 2000, siga los pasos que se enumeran a continuación para solucionar el problema.

1.  Asegúrese de que el servicio de publicación World Wide Web se está ejecutando primero navegando a https://*con* Internet Explorer. Si no puede obtener acceso al servidor Web, abra un símbolo del sistema o indicador de comandos y escriba el comando siguiente "NET START W3SVC".

2.  En el menú Inicio, seleccione Ejecutar. Escriba msdfmap.ini y haga clic en Aceptar para abrir el archivo msdfmap.ini en el Bloc de notas. Compruebe la sección CONNECT DEFAULT y, si el parámetro ACCESS está \[ \] establecido en NOACCESS, cámbie el parámetro a READONLY.

3.  Con la utilidad RegEdit, ve a "HKEY LOCAL MACHINE SOFTWARE Microsoft DataFactory HandlerInfo" y asegúrate de que HandlerRequired está establecido en 0 y \_ \_ \\ \\ \\ \\ **DefaultHandler** es "" (cadena Null). 
    
    > [!NOTE]
    > [!NOTA] Si realiza algunos cambios en esta sección del Registro, deberá detener y reiniciar el servicio de publicación Web escribiendo los comandos siguientes en un símbolo del sistema: "NET STOP W3SVC" y "NET START W3SVC".

4.  Mediante la utilidad RegEdit, navegue en el Registro a "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services \\ W3SVC Parameters ADCLaunch" y compruebe que hay una clave denominada \\ \\ **RDSServer.Datafactory**. Si no existe, créela.

5.  Con el Administrador de servicios de Internet, vaya al sitio web predeterminado y vea las propiedades de la raíz virtual de MSADC. Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio. Si está activada la opción "Acceso denegado", seleccione "Concedido".

Si los cambios no parecen solucionar el problema, intente reiniciar el servidor.

