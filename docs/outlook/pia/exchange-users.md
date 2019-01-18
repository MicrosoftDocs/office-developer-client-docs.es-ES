---
title: Usuarios de Exchange
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 667f8a07477c527d251c4e50f35baa2da2e417ed
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703226"
---
# <a name="exchange-users"></a>Usuarios de Exchange

Esta sección proporciona tareas de ejemplo que implican a los usuarios de correo de Microsoft Exchange. Los usuarios de Exchange están conectados a un servidor Exchange y se representan mediante los objetos [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) que se derivan del objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).

## <a name="in-this-section"></a>En esta sección

|Tema|Descripción|
|:----|:----------|
|[Obtener información sobre el usuario actual](how-to-get-information-about-the-current-user.md)  |Obtiene la información del usuario actual, como nombre, puesto y número de teléfono.|
|[Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |Usa el método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obtener información sobre todas las listas de distribución de las que el usuario actual es miembro.|
|[Crear una lista de distribución](how-to-create-a-distribution-list.md)  |Crea una lista de distribución y la muestra al usuario.|
[Obtener acceso a los miembros de una lista de distribución de Exchange](how-to-get-members-of-an-exchange-distribution-list.md)  |Solicita al usuario que seleccione una lista de distribución de Exchange del cuadro de diálogo **Seleccionar nombres** y expande la lista de distribución para mostrar sus miembros.|
[Obtener información sobre el administrador del usuario actual](how-to-get-information-about-the-current-user-s-manager.md)  |Obtiene información sobre el administrador del usuario actual (como nombre, puesto y números de teléfono).|
[Obtener información de disponibilidad de un administrador del usuario de Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  Muestra la franja de tiempo libre en los 60 minutos siguientes en el calendario de un administrador del usuario.|
|[Consultar la respuesta de un administrador a una convocatoria de reunión](how-to-check-a-manager-s-response-to-a-meeting-request.md) | Usa los métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) y [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para comprobar el estado de respuesta del administrador del usuario actual a una convocatoria de reunión.|
|[Obtener información sobre subordinados directos del administrador del usuario actual](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | Obtiene los subordinados directos del administrador del usuario actual, si existen, y muestra información sobre cada uno de ellos.|

## <a name="see-also"></a>Vea también

- [Cuentas](accounts.md)
- [Libreta de direcciones](address-book.md)
- [Stores](stores.md)
- [¿Cómo se puede... (Referencia a PIA de Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

