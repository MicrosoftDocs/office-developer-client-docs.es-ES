---
title: Configurar RDS en Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0aed6889f16d55ee3ba7778bf9acc6134b744c5d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602576"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="00530-102">Configurar RDS en Windows 2000</span><span class="sxs-lookup"><span data-stu-id="00530-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="00530-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00530-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00530-104">Si tiene dificultades para conseguir que RDS funcione correctamente tras actualizarse a Windows 2000, siga los pasos que se enumeran a continuación para solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="00530-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="00530-105">Asegúrese de que el servicio de publicación World Wide Web se está ejecutando primera navegando a https://*servidor* mediante el Explorador de Internet.</span><span class="sxs-lookup"><span data-stu-id="00530-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="00530-106">Si no puede obtener acceso al servidor Web, abra un símbolo del sistema o indicador de comandos y escriba el comando siguiente "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="00530-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="00530-107">En el menú Inicio, seleccione Ejecutar.</span><span class="sxs-lookup"><span data-stu-id="00530-107">From the Start menu, select Run.</span></span> <span data-ttu-id="00530-108">Escriba msdfmap.ini y haga clic en Aceptar para abrir el archivo msdfmap.ini en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="00530-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="00530-109">Comprobar la \[CONNECT DEFAULT\] sección y, si el parámetro de acceso se establece en NOACCESS, cámbielo a READONLY.</span><span class="sxs-lookup"><span data-stu-id="00530-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="00530-110">Uso de la utilidad RegEdit, vaya a "HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" y compruebe que **HandlerRequiredse** establece en 0 y **que DefaultHandler** es "" (Null cadena).</span><span class="sxs-lookup"><span data-stu-id="00530-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="00530-111">[!NOTA] Si realiza algunos cambios en esta sección del Registro, deberá detener y reiniciar el servicio de publicación Web escribiendo los comandos siguientes en un símbolo del sistema: "NET STOP W3SVC" y "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="00530-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span></P>



4.  <span data-ttu-id="00530-112">Utilizando RegEdit, desplácese en el registro para "HKEY\_LOCAL\_máquina\\SYSTEM\\CurrentControlSet\\servicios\\W3SVC\\parámetros\\ADCLaunch" y compruebe que haya una clave **llamado RDSServer.Datafactory**.</span><span class="sxs-lookup"><span data-stu-id="00530-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="00530-113">Si no existe, créela.</span><span class="sxs-lookup"><span data-stu-id="00530-113">If not, create it.</span></span>

<span data-ttu-id="00530-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="00530-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="00530-115">Mediante Internet Services Manager, vaya el sitio Web predeterminado y vea las propiedades de la raíz virtual MSADC.</span><span class="sxs-lookup"><span data-stu-id="00530-115">Using Internet Services Manager, go to the Default Web Site and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="00530-116">Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="00530-116">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="00530-117">Si está activada la opción "Acceso denegado", seleccione "Concedido".</span><span class="sxs-lookup"><span data-stu-id="00530-117">If the "Access is Denied" is checked then select "Granted".</span></span>
=======
5.  <span data-ttu-id="00530-118">Uso de administrador de servicios Internet, vaya al sitio Web predeterminado y ver las propiedades de la raíz virtual MSADC.</span><span class="sxs-lookup"><span data-stu-id="00530-118">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="00530-119">Inspeccione las restricciones de Seguridad de directorio/Dirección IP y Nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="00530-119">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="00530-120">Si está activada la opción "Acceso denegado", seleccione "Concedido".</span><span class="sxs-lookup"><span data-stu-id="00530-120">If the "Access is Denied" is checked then select "Granted".</span></span>
>>>>>>> <span data-ttu-id="00530-121">master</span><span class="sxs-lookup"><span data-stu-id="00530-121">master</span></span>

<span data-ttu-id="00530-122">Si los cambios no parecen solucionar el problema, intente reiniciar el servidor.</span><span class="sxs-lookup"><span data-stu-id="00530-122">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

