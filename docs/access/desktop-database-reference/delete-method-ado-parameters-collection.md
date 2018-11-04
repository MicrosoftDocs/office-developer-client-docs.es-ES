---
title: Método Delete (colección de parámetros de ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 213d29ecd6599803c0fa2211a17ac14da7dc698a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949456"
---
# <a name="delete-method-ado-parameters-collection"></a>Método Delete (colección de parámetros de ADO)

**Se aplica a**: Access 2013, Office 2013

Elimina un objeto de la colección [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Los parámetros*. Eliminar *índice*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Index* |Valor de tipo **String** que contiene el nombre del objeto que se va a eliminar, o bien, la posición ordinal (índice) del objeto en la colección.|

## <a name="remarks"></a>Comentarios

El uso del método **Delete** en una colección permite quitar uno de los objetos de la colección. Este método está disponible solo en la colección **Parameters** de un objeto [Command](command-object-ado.md). Debe usar la propiedad [Name](parameter-object-ado.md) del objeto [Parameter](name-property-ado.md) o su índice de colección al llamar al método **Delete**; una variable de objeto no es un argumento válido.

