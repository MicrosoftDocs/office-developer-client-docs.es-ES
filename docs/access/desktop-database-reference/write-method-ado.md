---
title: 'Método Write: ActiveX data objects (ADO)'
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302467"
---
# <a name="write-method-ado"></a>Método Write (ADO)

**Se aplica a:** Access 2013, Office 2013

Escribe datos binarios en un objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Stream*. Búfer de *escritura*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Buffer* |**Variant** que contiene la matriz de bytes que se va a escribir.|

## <a name="remarks"></a>Comentarios

Los bytes especificados se escriben en el objeto **Stream** sin espacios intermedios entre ellos.

El valor de [Position](position-property-ado.md) actual está establecido en el byte situado después de los datos escritos. El método **Write** no trunca el resto de los datos en una secuencia. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).

Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) del objeto **Stream** se incrementará para que pueda contener los bytes nuevos, y **EOS** se moverá hasta el último byte nuevo en el objeto **Stream**.

> [!NOTE]
> El método **Write** se utiliza con secuencias binarias (el valor de [Type](type-property-ado-stream.md) es **adTypeBinary**). Utilice [WriteText](writetext-method-ado.md) para las secuencias de texto (el valor de **Type** es **adTypeText**).

