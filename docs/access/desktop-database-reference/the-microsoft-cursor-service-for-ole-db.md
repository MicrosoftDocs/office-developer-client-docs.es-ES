---
title: El servicio de cursores de Microsoft para OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314360"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Servicio de cursores de Microsoft para OLE DB


**Se aplica a:** Access 2013, Office 2013

Cuando selecciona un cursor en el cliente o establece la propiedad **CursorLocation** en **adUseClient**, está invocando el servicio de cursores de Microsoft para OLE DB. También puede ver referencias a "Client Cursor Engine" (Motor de cursores clientes) que, en esencia, es lo mismo en el contexto de ADO. Este servicio complementa las funciones de soporte de cursores de los proveedores de datos. En consecuencia, se puede percibir una funcionalidad relativamente uniforme de todos los proveedores de datos.

Con el servicio de cursor para OLE DB, las propiedades dinámicas están disponibles y el comportamiento de ciertos métodos mejora. Por ejemplo, la propiedad dinámica **Optimizar** habilita a la creación de índices temporales para facilitar determinadas operaciones, como el método **Find**.

El servicio de cursor habilita la compatibilidad con la actualización por lotes en todos los casos. También simula tipos de cursor más capaces, como los cursores dinámicos, cuando un proveedor de datos sólo puede suministrar cursores menos capaces, como cursores estáticos.

