---
title: Delete (método, colección paraMeters de ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294095"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete (método, colección paraMeters de ADO)

**Se aplica a:** Access 2013, Office 2013

Elimina un objeto de la colección [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Parámetros*. Eliminar *Índice*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Index* |Valor de tipo **String** que contiene el nombre del objeto que se va a eliminar, o bien, la posición ordinal (índice) del objeto en la colección.|

## <a name="remarks"></a>Comentarios

El uso del método **Delete** en una colección permite quitar uno de los objetos de la colección. Este método está disponible solo en la colección **Parameters** de un objeto [Command](command-object-ado.md). Debe usar la propiedad [Name](name-property-ado.md) del objeto [Parameter](parameter-object-ado.md) o su índice de colección al llamar al método **Delete**; una variable de objeto no es un argumento válido.

