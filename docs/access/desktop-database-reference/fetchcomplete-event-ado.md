---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293192"
---
# <a name="fetchcomplete-event-ado"></a>Evento FetchComplete (ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **FetchComplete** se le llama después de que todos los registros en una operación asincrónica prolongada se hayan recuperado e insertado en el objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

FetchComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pRecordset* |Objeto **Recordset**. El objeto para el que se recuperaron los registros.|

## <a name="remarks"></a>Comentarios

Para utilizar **FetchComplete** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.

