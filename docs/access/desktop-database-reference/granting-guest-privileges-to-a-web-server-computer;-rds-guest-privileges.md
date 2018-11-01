---
title: Conceder privilegios de invitado a un equipo de servidor Web; Privilegios de invitado RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed450913c7512e8ef20983484ca4b874878fd791
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867170"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="27910-102">Conceder privilegios de invitado a un equipo de servidor Web; Privilegios de invitado RDS</span><span class="sxs-lookup"><span data-stu-id="27910-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="27910-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27910-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27910-104">La cuenta del servidor web anónimo (IUSR\_*ComputerName*) debe agregarse al grupo local invitados en el equipo servidor web para utilizar RDS.</span><span class="sxs-lookup"><span data-stu-id="27910-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="27910-105">**Para conceder privilegios de invitado a un equipo servidor web**</span><span class="sxs-lookup"><span data-stu-id="27910-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="27910-106">En su equipo con Microsoft Windows ® 2000 Server, haga clic en **Inicio**, elija **Programas**, \*\* Herramientas administrativas\*\* y haga clic en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="27910-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="27910-107">En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="27910-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="27910-p101">Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="27910-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="27910-110">En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="27910-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="27910-111">Si la cuenta del servidor web anónimo no aparece en la lista en el cuadro de diálogo **Seleccionar usuarios o grupos** , escriba su nombre (IUSR\_*ComputerName*) en la parte inferior en blanco cuadro y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="27910-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="27910-112">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="27910-112">Click **OK**.</span></span>

