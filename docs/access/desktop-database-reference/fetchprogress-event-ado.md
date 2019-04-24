---
title: FetchProgress (evento, ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293185"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress (evento, ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **FetchProgress** se le llama periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se han recuperado e insertado actualmente en el objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

FetchProgress** Progress, *MaxProgress*, adStatus, *pRecordset* **

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Progress* |Valor **Long** que indica el número de registros que han sido recuperados actualmente por la operación de búsqueda.|
|*MaxProgress* |Valor **Long** que indica el número máximo de registros que se espera recuperar.|
|*adStatus* |Valor de estado [EventStatusEnum](eventstatusenum.md).|
|*pRecordset* |Objeto **Recordset** para el que se están recuperando los registros.|

## <a name="remarks"></a>Comentarios

Cuando use **FetchProgress** con un objeto **Recordset** secundario, tenga en cuenta que los valores de los parámetros *Progress* y *MaxProgress* se obtienen del conjunto de filas del [Servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) subyacente. Los valores devueltos representan el número total de registros en el conjunto de filas subyacente, no solo el número de registros en el capítulo actual.

> [!NOTE]
> [!NOTA] Para utilizar **FetchProgress** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.


