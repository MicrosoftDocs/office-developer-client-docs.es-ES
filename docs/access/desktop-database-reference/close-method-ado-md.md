---
title: Close (método, ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28c5ff23470015c9b40c996a1eb5b60f74766da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888793"
---
# <a name="close-method-ado-md"></a>Close (método, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Cierra un conjunto de celdas abierto.

## <a name="syntax"></a>Sintaxis

*Conjunto de celdas*. Cerrar

## <a name="remarks"></a>Comentarios

Si se usa el método **Close** para cerrar un objeto [Cellset](cellset-object-ado-md.md), se liberarán los datos asociados, incluidos los datos de todo objeto [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) o [Member](member-object-ado-md.md) relacionado. El hecho de cerrar un **conjunto de celdas** no lo borra de la memoria; puede cambiar la configuración de sus propiedades y abrirlo de nuevo más tarde. Para eliminar completamente un objeto de la memoria, establezca la variable del objeto en **Nothing**.

Puede llamar posteriormente al método [Open](open-method-ado-md.md) para volver a abrir el **conjunto de celdas** utilizando la misma cadena de origen u otra. Si, mientras se cierra el objeto **Cellset**, se recuperan propiedades o se llama a algún método que haga referencia a los datos o metadatos subyacentes, se producirá un error.

