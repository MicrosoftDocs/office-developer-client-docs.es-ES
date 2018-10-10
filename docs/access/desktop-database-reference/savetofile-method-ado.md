---
title: SaveToFile (método, ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0bd915a4eb6405b7d5ddd4bfe42eb4a98f68b89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483940"
---
# <a name="savetofile-method-ado"></a>SaveToFile (método, ADO)


**Se aplica a**: Access 2013 | Office 2013



Guarda el contenido binario de un objeto [Stream](stream-object-ado.md) en un archivo.

## <a name="syntax"></a>Sintaxis

*Secuencia*. SaveToFile*FileName*, *SaveOptions*

## <a name="parameters"></a>Parámetros

  - *FileName*

  - Valor de tipo **String** que contiene el nombre completo del archivo en el que se va a guardar el contenido del objeto **Stream**. Se puede guardar en cualquier ubicación local válida o cualquier ubicación a la que se tenga acceso mediante un valor UNC.

  - *SaveOptions*

  - Valor de [SaveOptionsEnum](saveoptionsenum.md) que especifica si **SaveToFile** debe crear un archivo nuevo si aún no existe. El valor predeterminado es **adSaveCreateNotExists**. Con estas opciones, se puede especificar que se genere un error si no existe el archivo indicado. Asimismo, se puede especificar que **SaveToFile** sobrescriba el contenido de un archivo existente.


> [!NOTE]
> <P>[!NOTA] Si se sobrescribe un archivo existente (cuando se ha establecido el valor <STRONG>adSaveCreateOverwrite</STRONG> ), <STRONG>SaveToFile</STRONG> truncará los bytes del archivo existente original que aparezcan después del nuevo <A href="eos-property-ado.md">EOS</A>.</P>



## <a name="remarks"></a>Comentarios

**SaveToFile** puede utilizarse para copiar el contenido de un objeto **Stream** en un archivo local. No se produce ningún cambio en el contenido ni en las propiedades del objeto **Stream**. El objeto **Stream** debe estar abierto antes de que se llame a **SaveToFile**.

Este método no cambia la asociación del objeto **Stream** a su origen subyacente. El objeto **Stream** permanecerá asociado a la dirección URL original o al objeto **Record** que era su origen al abrirse.

Después de una operación de **SaveToFile**, la posición actual ([Position](position-property-ado.md)) en la secuencia se establece en el principio de la secuencia (0).

