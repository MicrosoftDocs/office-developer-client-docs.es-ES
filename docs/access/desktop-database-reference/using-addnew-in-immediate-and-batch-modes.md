---
title: Utilizar AddNew en modos Inmediato y Proceso por lotes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b37acc1819d12acc1e659be85361c3c09b84ebdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484364"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Utilizar AddNew en modos Inmediato y Proceso por lotes


**Se aplica a**: Access 2013 | Office 2013

El comportamiento del método **AddNew** depende del modo de actualización del objeto **Recordset** y si se pasan los argumentos *FieldList* y *Values* .

En modo de actualización inmediata (en el que el proveedor escribe los cambios en el origen de datos subyacente una vez que se ha llamado al método **Update**), si se llama al método **AddNew** sin argumentos, la propiedad **EditMode** se establece en **adEditAdd**. El proveedor almacena en caché localmente los cambios de valor de campo. Si se llama al método **Update**, se envía el nuevo registro a la base de datos y se restablece la propiedad **EditMode** en **adEditNone**. Si pasa los argumentos *FieldList* y *Values*, ADO envía inmediatamente el nuevo registro a la base de datos (sin necesidad de una llamada a **Update**); el valor de la propiedad **EditMode** no cambia (**adEditNone**).

En modo de actualización por lotes, si se llama al método **AddNew** sin argumentos, la propiedad **EditMode** se establece en **adEditAdd**. El proveedor almacena en caché localmente los cambios de valor de campo. Si se llama al método **Update**, el nuevo registro se agrega al **conjunto de registros** activo y la propiedad **EditMode** se restablece en **adEditNone**, pero el proveedor no envía los cambios a la base de datos subyacente hasta que se llame al método **UpdateBatch**. Si se pasan los argumentos *FieldList* y *Values* , ADO envía el nuevo registro al proveedor para el almacenamiento en caché; debe llamar al método **UpdateBatch** para enviar el nuevo registro a la base de datos subyacente. Para obtener más información acerca de **Update** y **UpdateBatch**, vea [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).

