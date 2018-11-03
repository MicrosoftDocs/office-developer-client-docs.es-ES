---
title: Método Delete (colección de campos de ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afeec4007b9bd44a9575217e1fb6380a50d699c3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945320"
---
# <a name="delete-method-ado-fields-collection"></a>Método Delete (colección de campos de ADO)


**Se aplica a**: Access 2013, Office 2013



Elimina un objeto de la colección [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Los campos*. Eliminar*campo*

## <a name="parameters"></a>Parámetros

- *Field*

  - **Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.

## <a name="remarks"></a>Comentarios

Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.

