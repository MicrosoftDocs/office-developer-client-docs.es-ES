---
title: Conceder privilegios de invitado a un equipo de servidor web; Privilegios de invitado RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1f127e4ea9393d3b461e9b7da2901df554ee36b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947213"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="ff090-102">Conceder privilegios de invitado a un equipo de servidor web; Privilegios de invitado RDS</span><span class="sxs-lookup"><span data-stu-id="ff090-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="ff090-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff090-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff090-104">La cuenta del servidor web anónimo (IUSR\_*ComputerName*) debe agregarse al grupo local invitados en el equipo servidor web para utilizar RDS.</span><span class="sxs-lookup"><span data-stu-id="ff090-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="ff090-105">**Para conceder privilegios de invitado a un equipo servidor web**</span><span class="sxs-lookup"><span data-stu-id="ff090-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="ff090-106">En el equipo de Microsoft Windows 2000 Server, haga clic en **Inicio**, elija **programas**, elija **Herramientas administrativas**y, a continuación, haga clic en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="ff090-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="ff090-107">En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="ff090-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="ff090-p101">Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ff090-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="ff090-110">En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ff090-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="ff090-111">Si la cuenta del servidor web anónimo no aparece en la lista en el cuadro de diálogo **Seleccionar usuarios o grupos** , escriba su nombre (IUSR\_*ComputerName*) en la parte inferior en blanco cuadro y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ff090-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="ff090-112">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff090-112">Click **OK**.</span></span>

