---
title: CancelarCambioDeRegistro (acción de macro)
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718546"
---
# <a name="cancelrecordchange-macro-action"></a>CancelarCambioDeRegistro (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)** antes de que se confirmen los cambios.


> [!NOTE]
> [!NOTA] La acción **CancelarCambioDeRegistro** solo está disponible en macros de datos.



## <a name="remarks"></a>Comentarios

Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.

