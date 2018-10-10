---
title: Delete (método, colección Fields de ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485301"
---
# <a name="delete-method-ado-fields-collection"></a>Delete (método, colección Fields de ADO)


**Se aplica a**: Access 2013 | Office 2013



Elimina un objeto de la colección [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Los campos*. Eliminar*campo*

## <a name="parameters"></a>Parámetros

  - *Field*

  - **Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.

## <a name="remarks"></a>Comentarios

Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.

