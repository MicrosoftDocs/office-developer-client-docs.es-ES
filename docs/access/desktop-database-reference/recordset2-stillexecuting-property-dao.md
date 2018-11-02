---
title: Propiedad Recordset2.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55a5adf32c64735cb773e3f1da5de79703a2a3cc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930150"
---
# <a name="recordset2stillexecuting-property-dao"></a>Propiedad Recordset2.StillExecuting (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . StillExecuting

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Utilice la propiedad **StillExecuting** para determinar si el método asincrónico **Execute** o **OpenConnection** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se ha completado. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.

Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **Connection**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.

Utilice el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea que se esté realizando.

