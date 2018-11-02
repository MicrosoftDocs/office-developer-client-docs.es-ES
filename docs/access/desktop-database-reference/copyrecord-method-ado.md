---
title: CopyRecord (método, ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f25d3f7cb576a9fb8ddf79a887bb3c795144682
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919034"
---
# <a name="copyrecord-method-ado"></a>CopyRecord (método, ADO)


**Se aplica a**: Access 2013, Office 2013

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

## <a name="return-value"></a>Valor devuelto

Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.

## <a name="remarks"></a>Comentarios

Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución. Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.

Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.

Este método se produce un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que **se especifique adCopyOverWrite** .


> [!IMPORTANT]
> [!IMPORTANTE] Utilice la opción **adCopyOverWrite** con criterio. Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio va a *Eliminar* el directorio y reemplácelo con el archivo.




> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


