---
title: CopyRecord (método, ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73940108f96cf46cb15d646936039c0329373899
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606909"
---
# <a name="copyrecord-method-ado"></a>CopyRecord (método, ADO)


**Se aplica a**: Access 2013 | Office 2013

Copia una entidad representada por un objeto **Record** en otra ubicación.

## <a name="syntax"></a>Sintaxis

*Registro*. CopyRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)

## <a name="parameters"></a>Parámetros

  - *Source*

  - Es opcional. Valor de tipo **String** con la dirección URL que especifica la entidad que se va a copiar (por ejemplo, un archivo o directorio). Si se omite *Source* o especifica una cadena vacía, se copiará el archivo o directorio representado por el actual [registro](record-object-ado.md) .

  - *Destination*

  - Es opcional. Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a copiar *Source* .

  - *UserName*

  - Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.

  - *Password*

  - Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.

  - *Options*

  - Es opcional. Valor de [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tiene **adCopyUnspecified** como valor predeterminado. Especifica el comportamiento de este método.

  - *Async*

  - Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.

## <a name="remarks"></a>Comentarios

Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución. Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.

Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.

Este método se produce un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que **se especifique adCopyOverWrite** .


> [!IMPORTANT]
> <P>[!IMPORTANTE] Utilice la opción <STRONG>adCopyOverWrite</STRONG> con criterio. Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio va a <EM>Eliminar</EM> el directorio y reemplácelo con el archivo.</P>




> [!NOTE]
<<<<<<< HEAD
> <P>[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</P>
=======
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).
>>>>>>> master


