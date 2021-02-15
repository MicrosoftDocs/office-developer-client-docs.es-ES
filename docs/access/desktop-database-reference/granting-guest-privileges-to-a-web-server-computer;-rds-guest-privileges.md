---
title: Conceder privilegios de invitado a un equipo servidor web; Privilegios de invitado de RDS
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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Conceder privilegios de invitado a un equipo servidor web; Privilegios de invitado de RDS

**Se aplica a:** Access 2013, Office 2013

La cuenta de servidor web anónimo (IUSR \_ *ComputerName)* debe agregarse al grupo local Invitados en el equipo servidor web para usar RDS.

**Para conceder privilegios de invitado a un equipo servidor web**

1.  En el equipo con Microsoft Windows 2000 Server, haga clic en Inicio **,** seleccione **Programas,** Herramientas administrativas y, a continuación, haga clic en Administración **de equipos.**

2.  En el árbol de la consola, en **Usuarios locales y grupos**, haga clic en **Grupos**.

3.  Seleccione el grupo local **Invitados**. En el menú **Acción**, elija **Propiedades**.

4.  En el cuadro de diálogo **Propiedades de Invitados**, haga clic en **Agregar**.

5.  Si la cuenta de servidor web anónimo  no aparece en la lista del cuadro de diálogo Seleccionar usuarios o grupos, escriba su nombre (IUSR \_ *ComputerName)* en el cuadro en blanco inferior y, a continuación, haga clic en Agregar . 

6.  Haga clic en **Aceptar**.

