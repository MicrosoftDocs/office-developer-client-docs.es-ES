---
title: FetchComplete (evento, ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485403"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete (evento, ADO)


**Se aplica a**: Access 2013 | Office 2013


Al evento **FetchComplete** se le llama después de que todos los registros en una operación asincrónica prolongada se hayan recuperado e insertado en el objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

FetchComplete*pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *pError*

  - Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.

  - *Connection*

  - Objeto **Recordset**. El objeto para el que se recuperaron los registros.

## <a name="remarks"></a>Comentarios

Para utilizar **FetchComplete** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.

