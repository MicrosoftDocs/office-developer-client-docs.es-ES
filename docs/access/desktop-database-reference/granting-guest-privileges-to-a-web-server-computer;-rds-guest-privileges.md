---
title: Conceder privilegios de invitado a un equipo de servidor Web; Privilegios de invitado RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d09de280c9edcfdf4305bb6c2ba09aa01e556ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485296"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="97d07-102">Conceder privilegios de invitado a un equipo de servidor Web; Privilegios de invitado RDS</span><span class="sxs-lookup"><span data-stu-id="97d07-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="97d07-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97d07-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="97d07-104">La cuenta anónima de servidor Web (IUSR\_*ComputerName*) debe agregarse al grupo local invitados en el equipo servidor Web para utilizar RDS.</span><span class="sxs-lookup"><span data-stu-id="97d07-104">The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<span data-ttu-id="97d07-105">**Para conceder privilegios de invitado a un equipo de servidor Web**</span><span class="sxs-lookup"><span data-stu-id="97d07-105">**To grant guest privileges to a Web server computer**</span></span>

1.  <span data-ttu-id="97d07-106">En su equipo con Microsoft Windows ® 2000 Server, haga clic en **Inicio**, elija **Programas**, \*\* Herramientas administrativas\*\* y haga clic en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="97d07-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="97d07-107">En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="97d07-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="97d07-p101">Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="97d07-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="97d07-110">En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="97d07-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="97d07-111">Si la cuenta anónima de servidor Web no aparece en la lista en el cuadro de diálogo **Seleccionar usuarios o grupos** , escriba su nombre (IUSR\_*ComputerName*) en la parte inferior en blanco cuadro y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="97d07-111">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="97d07-112">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="97d07-112">Click **OK**.</span></span>

