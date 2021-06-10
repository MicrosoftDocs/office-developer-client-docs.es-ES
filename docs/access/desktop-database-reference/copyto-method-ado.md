---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295481"
---
# <a name="copyto-method-ado"></a>Método CopyTo (ADO)

**Se aplica a:** Access 2013, Office 2013

Copia el número especificado de caracteres o bytes (según [Type](type-property-ado-stream.md)) de un objeto [Stream](stream-object-ado.md) a otro objeto **Stream**.

## <a name="syntax"></a>Sintaxis

*Stream*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DestStream* |Valor de variable de objeto que contiene una referencia a un objeto **Stream** abierto. El actual objeto **Stream** se copia en el objeto **Stream** de destino especificado por *DestStream*. El objeto **Stream** de destino ya debe estar abierto. De lo contrario, se produce un error en tiempo de ejecución.

<br/><br/>**NOTA**: Es posible que el parámetro *DestStream* no sea un proxy del objeto **Stream,** ya que requiere acceso a una interfaz privada en el **objeto Stream** que no se puede remotar en el cliente.|
|*NumChars* |Es opcional. Valor de tipo **Integer** que especifica el número de bytes o caracteres que se van a copiar a partir de la actual posición en el objeto **Stream** de origen al objeto **Stream** de destino. El valor predeterminado es –1, que especifica que se van a copiar todos los caracteres o bytes desde la posición actual hasta [EOS](eos-property-ado.md).|

## <a name="remarks"></a>Comentarios

Este método copia el número especificado de caracteres o bytes, a partir de la actual posición especificada por la propiedad [Position](position-property-ado.md). Si el número especificado es mayor que el número de bytes disponibles hasta **EOS**, sólo se copiarán los caracteres o bytes desde la posición actual hasta **EOS**. Si el valor de *NumChars* es –1 o se omite, se copiarán todos los caracteres o bytes a partir de la posición actual.

Si hay caracteres o bytes en la secuencia de destino, se mantiene todo el contenido situado más allá del punto donde finaliza la copia y no se ve truncado. El valor de **Position** será el byte inmediatamente después del último byte copiado. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).

**CopyTo** debe utilizarse para copiar datos a un objeto **Stream** de destino del mismo tipo que el objeto **Stream** de origen (el valor de la propiedad **Type** de ambos objetos debe ser **adTypeText** o **adTypeBinary**). Para los objetos **Stream** de texto, puede cambiar la configuración de la propiedad [Charset](charset-property-ado.md) del objeto **Stream** de destino para permitir la conversión de un juego de caracteres a otro. Además, los objetos **Stream** de texto se pueden copiar correctamente a los objetos **Stream** binarios,pero no a lainversa.

