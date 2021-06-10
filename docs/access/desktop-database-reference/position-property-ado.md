---
title: Propiedad Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287527"
---
# <a name="position-property-ado"></a>Propiedad Position (ADO)

**Se aplica a:** Access 2013, Office 2013

Indica la posición actual dentro de un objeto [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que especifica el desplazamiento, en número de bytes, de la posición actual desde el principio de la secuencia. El valor predeterminado es 0, que representa el primer byte de la secuencia.

## <a name="remarks"></a>Comentarios

La posición actual puede moverse a un punto situado detrás del final de la secuencia. Si se especifica la posición actual detrás del fin de la secuencia, el [tamaño](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) del objeto **Stream** aumentará en consecuencia. Cualquier byte nuevo agregado de esta forma será nulo.

> [!NOTE]
> [!NOTA] **Position** siempre mide bytes. En las secuencias de texto que usan juegos de caracteres multibyte, multiplique la posición por el tamaño de los caracteres para determinar el número de caracteres. Por ejemplo, en un juego de caracteres de dos bytes, el primer carácter se encuentra en la posición 0, el segundo en la 2, el tercero en la 4 y así sucesivamente.

No es posible utilizar valores negativos para cambiar la posición actual en un objeto **Stream**. Con **Position** sólo se pueden utilizar números positivos.

En los objetos **Stream** de sólo lectura, ADO no devolverá un error si **Position** se establece en un valor superior al **tamaño** de **Stream**. Eso no modifica el tamaño de **Stream** ni altera el contenido de **Stream** de ninguna forma. Sin embargo, debe evitarse, ya que da lugar a un valor de **Position** sin sentido.

