---
title: CancelarCambioDeRegistro (acción de macro)
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddf6a6eb71d60fb98d92a9ce18bfd871f298f702
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864210"
---
# <a name="cancelrecordchange-macro-action"></a>CancelarCambioDeRegistro (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)** antes de que se confirmen los cambios.


> [!NOTE]
> [!NOTA] La acción **CancelarCambioDeRegistro** solo está disponible en macros de datos.



## <a name="remarks"></a>Comentarios

Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.

