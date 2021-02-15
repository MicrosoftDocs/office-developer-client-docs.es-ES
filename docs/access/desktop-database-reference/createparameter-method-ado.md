---
title: Método CreateParameter (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295397"
---
# <a name="createparameter-method-ado"></a>Método CreateParameter (ADO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto [Parameter](parameter-object-ado.md) con las propiedades especificadas.

## <a name="syntax"></a>Sintaxis

**Establecer comando** *de*  =  *parámetro*. CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto **Parameter**.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Name* |Es opcional. Valor de tipo **String** que contiene el nombre del objeto **Parameter**.|
|*Type* |Es opcional. Valor de [DataTypeEnum](datatypeenum.md) que especifica el tipo de datos del objeto **Parameter**.|
|*Direction* |Es opcional. Valor de [ParameterDirectionEnum](parameterdirectionenum.md) que especifica el tipo del objeto **Parameter**.|
|*Size* |Es opcional. Valor de tipo **Long** que especifica la longitud máxima del valor de parámetro, en caracteres o bytes.|
|*Valor* |Es opcional. **Variant** que especifica el valor del objeto **Parameter**.|

## <a name="remarks"></a>Comentarios

Utilice el método **CreateParameter** para crear un nuevo objeto **Parameter** con un nombre, un tipo, una dirección, un tamaño y un valor especificados. Cualquier valor que pase en los argumentos se escribe en las correspondientes propiedades de **Parameter**.

Este método no anexa automáticamente el objeto **Parameter** a la colección **Parameters** de un objeto [Command](command-object-ado.md). Esto le permite establecer propiedades adicionales cuyos valores ADO validará cuando se anexe el objeto **Parameter** a la colección.

Si especifica un tipo de datos de longitud variable en el argumento *Type*, deberá pasar un argumento *Size* o establecer la propiedad [Size](size-property-ado.md) del objeto **Parameter** antes de anexarlo a la colección **Parámetros**.

Si especifica un tipo de datos numérico (**adNumeric** o **adDecimal**) en el argumento *Type*, también deberá establecer las propiedades [NumericScale](numericscale-property-ado.md) y [Precision](precision-property-ado.md).

