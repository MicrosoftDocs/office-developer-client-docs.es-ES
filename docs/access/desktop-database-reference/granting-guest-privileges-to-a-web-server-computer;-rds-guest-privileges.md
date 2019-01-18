---
title: Conceder privilegios de invitado a un equipo de servidor web; Privilegios de invitado RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700552"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Conceder privilegios de invitado a un equipo de servidor web; Privilegios de invitado RDS

**Se aplica a**: Access 2013, Office 2013

La cuenta del servidor web anónimo (IUSR\_*ComputerName*) debe agregarse al grupo local invitados en el equipo servidor web para utilizar RDS.

**Para conceder privilegios de invitado a un equipo servidor web**

1.  En el equipo de Microsoft Windows 2000 Server, haga clic en **Inicio**, elija **programas**, elija **Herramientas administrativas**y, a continuación, haga clic en **Administración de equipos**.

2.  En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.

3.  Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.

4.  En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.

5.  Si la cuenta del servidor web anónimo no aparece en la lista en el cuadro de diálogo **Seleccionar usuarios o grupos** , escriba su nombre (IUSR\_*ComputerName*) en la parte inferior en blanco cuadro y, a continuación, haga clic en **Agregar**.

6.  Haga clic en **Aceptar**.

