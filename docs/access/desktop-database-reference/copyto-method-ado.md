---
title: CopyTo (método, ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bd949b92068619b76ac78d5e62cde0e247ed7b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484748"
---
# <a name="copyto-method-ado"></a>CopyTo (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Copia el número especificado de caracteres o bytes (según [Type](type-property-ado-stream.md)) de un objeto [Stream](stream-object-ado.md) a otro objeto **Stream**.

## <a name="syntax"></a>Sintaxis

*Secuencia*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Parámetros

  - *DestStream*

  - Valor de variable de objeto que contiene una referencia a un objeto **Stream** abierto. El actual objeto **Stream** se copia en el objeto **Stream** de destino especificado por *DestStream*. El objeto **Stream** de destino ya debe estar abierto. De lo contrario, se produce un error en tiempo de ejecución.


    

    > [!NOTE]
    > <P>El parámetro <EM>DestStream</EM> puede no ser un proxy del objeto <STRONG>Stream</STRONG> porque esto requiere acceso a una interfaz privada en el objeto <STRONG>Stream</STRONG> que no puede ser remoto para el cliente.</P>



  - *NumChars*

  - Es opcional. Valor de tipo **Integer** que especifica el número de bytes o caracteres que se van a copiar a partir de la actual posición en el objeto **Stream** de origen al objeto **Stream** de destino. El valor predeterminado es – 1, que especifica que todos los caracteres o bytes se copian desde la posición actual hasta [EOS](eos-property-ado.md).

## <a name="remarks"></a>Comentarios

Este método copia el número especificado de caracteres o bytes, a partir de la actual posición especificada por la propiedad [Position](position-property-ado.md). Si el número especificado es mayor que el número de bytes disponibles hasta **EOS**, sólo se copiarán los caracteres o bytes desde la posición actual hasta **EOS**. Si el valor de *NumChars* es – 1 o se omite, se copiarán todos los caracteres o bytes a partir de la posición actual.

Si hay caracteres o bytes en la secuencia de destino, se mantiene todo el contenido situado más allá del punto donde finaliza la copia y no se ve truncado. El valor de **Position** será el byte inmediatamente después del último byte copiado. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).

**CopyTo** debe utilizarse para copiar datos a un objeto **Stream** de destino del mismo tipo que el objeto **Stream** de origen (el valor de la propiedad **Type** de ambos objetos debe ser **adTypeText** o **adTypeBinary**). Para los objetos **Stream** de texto, puede cambiar la configuración de la propiedad [Charset](charset-property-ado.md) del objeto **Stream** de destino para permitir la conversión de un juego de caracteres a otro. Además, los objetos **Stream** de texto se pueden copiar correctamente a los objetos **Stream** binarios,**** pero no a la**** inversa.

