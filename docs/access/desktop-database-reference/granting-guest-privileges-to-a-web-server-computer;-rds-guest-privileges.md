---
title: Concesión de privilegios de invitado a un equipo servidor web; Privilegios de invitado de RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292128"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="ec227-102">Concesión de privilegios de invitado a un equipo servidor web; Privilegios de invitado de RDS</span><span class="sxs-lookup"><span data-stu-id="ec227-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="ec227-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec227-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec227-104">La cuenta de servidor web anónimo (IUSR ComputerName ) debe agregarse al grupo local Invitados en el equipo servidor web para \_ usar RDS.</span><span class="sxs-lookup"><span data-stu-id="ec227-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="ec227-105">**Para conceder privilegios de invitado a un equipo servidor web**</span><span class="sxs-lookup"><span data-stu-id="ec227-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="ec227-106">En el equipo de Microsoft Windows 2000 Server, haga clic en Inicio **,** seleccione Programas **,** Herramientas administrativas y, a continuación, haga clic en Administración **del equipo**.</span><span class="sxs-lookup"><span data-stu-id="ec227-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="ec227-107">En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="ec227-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="ec227-p101">Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ec227-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="ec227-110">En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ec227-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="ec227-111">Si la cuenta de servidor web anónimo  no aparece en la lista del cuadro de diálogo Seleccionar usuarios o grupos, escriba su nombre (IUSR \_ *ComputerName*) en el cuadro en blanco inferior y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ec227-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="ec227-112">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ec227-112">Click **OK**.</span></span>

