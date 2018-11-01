---
title: Delete (método, colección Fields de ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886399"
---
# <a name="delete-method-ado-fields-collection"></a>Delete (método, colección Fields de ADO)


**Se aplica a**: Access 2013, Office 2013



Elimina un objeto de la colección [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Los campos*. Eliminar*campo*

## <a name="parameters"></a>Parámetros

  - *Field*

  - **Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.

## <a name="remarks"></a>Comentarios

Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.

