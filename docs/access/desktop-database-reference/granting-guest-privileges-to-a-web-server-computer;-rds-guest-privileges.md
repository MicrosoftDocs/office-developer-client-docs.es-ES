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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Conceder privilegios de invitado a un equipo de servidor Web; Privilegios de invitado RDS 


**Se aplica a**: Access 2013 | Office 2013

La cuenta anónima de servidor Web (IUSR\_*ComputerName*) debe agregarse al grupo local invitados en el equipo servidor Web para utilizar RDS.

**Para conceder privilegios de invitado a un equipo de servidor Web**

1.  En su equipo con Microsoft Windows ® 2000 Server, haga clic en **Inicio**, elija **Programas**, ** Herramientas administrativas** y haga clic en **Administración de equipos**.

2.  En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.

3.  Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.

4.  En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.

5.  Si la cuenta anónima de servidor Web no aparece en la lista en el cuadro de diálogo **Seleccionar usuarios o grupos** , escriba su nombre (IUSR\_*ComputerName*) en la parte inferior en blanco cuadro y, a continuación, haga clic en **Agregar**.

6.  Haga clic en **Aceptar**.

