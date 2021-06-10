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
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="8b21e-102">Configuración de RDS en Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8b21e-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="8b21e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b21e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b21e-104">Si tiene dificultades para conseguir que RDS funcione correctamente tras actualizarse a Windows 2000, siga los pasos que se enumeran a continuación para solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="8b21e-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="8b21e-105">Asegúrese de que el servicio de publicación world wide web se ejecuta primero navegando a https://*con* Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8b21e-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="8b21e-106">Si no puede obtener acceso al servidor Web, abra un símbolo del sistema o indicador de comandos y escriba el comando siguiente "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="8b21e-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="8b21e-107">En el menú Inicio, seleccione Ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8b21e-107">From the Start menu, select Run.</span></span> <span data-ttu-id="8b21e-108">Escriba msdfmap.ini y haga clic en Aceptar para abrir el archivo msdfmap.ini en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="8b21e-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="8b21e-109">Compruebe la sección CONNECT DEFAULT y, si el parámetro ACCESS está \[ \] establecido en NOACCESS, cámbielo a READONLY.</span><span class="sxs-lookup"><span data-stu-id="8b21e-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="8b21e-110">Con la utilidad RegEdit, vaya a "HKEY LOCAL MACHINE SOFTWARE Microsoft DataFactory HandlerInfo" y asegúrese de que HandlerRequired está establecido en 0 y \_ \_ \\ \\ \\ \\ **DefaultHandler** es "" (cadena Null). </span><span class="sxs-lookup"><span data-stu-id="8b21e-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8b21e-111">[!NOTA] Si realiza algunos cambios en esta sección del Registro, deberá detener y reiniciar el servicio de publicación Web escribiendo los comandos siguientes en un símbolo del sistema: "NET STOP W3SVC" y "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="8b21e-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="8b21e-112">Con la utilidad RegEdit, navegue en el Registro a "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services \\ W3SVC Parameters ADCLaunch" y compruebe que hay una clave denominada \\ \\ **RDSServer.Datafactory**.</span><span class="sxs-lookup"><span data-stu-id="8b21e-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="8b21e-113">Si no existe, créela.</span><span class="sxs-lookup"><span data-stu-id="8b21e-113">If not, create it.</span></span>

5.  <span data-ttu-id="8b21e-114">Con Internet Services Manager, vaya al sitio web predeterminado y vea las propiedades de la raíz virtual de MSADC.</span><span class="sxs-lookup"><span data-stu-id="8b21e-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="8b21e-115">Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="8b21e-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="8b21e-116">Si está activada la opción "Acceso denegado", seleccione "Concedido".</span><span class="sxs-lookup"><span data-stu-id="8b21e-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="8b21e-117">Si los cambios no parecen solucionar el problema, intente reiniciar el servidor.</span><span class="sxs-lookup"><span data-stu-id="8b21e-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

