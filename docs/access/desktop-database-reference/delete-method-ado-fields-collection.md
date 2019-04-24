---
title: Delete (método, colección Fields de ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294109"
---
# <a name="delete-method-ado-fields-collection"></a>Delete (método, colección Fields de ADO)

**Se aplica a:** Access 2013, Office 2013


Elimina un objeto de la colección [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Campos*. Eliminar*campo*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Field* |**Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.|

## <a name="remarks"></a>Comentarios

Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.

