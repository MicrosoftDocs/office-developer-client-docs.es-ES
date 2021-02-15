---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295530"
---
# <a name="copyrecord-method-ado"></a>Método CopyRecord (ADO)

**Se aplica a:** Access 2013, Office 2013

Copia una entidad representada por un objeto **Record** en otra ubicación.

## <a name="syntax"></a>Sintaxis

*Record*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **String** con la dirección URL que especifica la entidad que se va a copiar (por ejemplo, un archivo o directorio). Si se omite *Source* o especifica una cadena vacía, se copiará el archivo o directorio representado por el actual objeto [Record](record-object-ado.md).|
|*Destination* |Es opcional. Valor de tipo **String** con la dirección URL que especifica la ubicación en la que se va a copiar *Source*.|
|*UserName* |Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.|
|*Password* |Opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.|
|*Options* |Es opcional. Valor de [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tiene **adCopyUnspecified** como valor predeterminado. Especifica el comportamiento de este método.|
|*Async* |Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.|

## <a name="return-value"></a>Valor devuelto

Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.

## <a name="remarks"></a>Comentarios

Los valores de *Source* y *Destination* no pueden ser idénticos; en caso contrario, se produce un error en tiempo de ejecución. Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.

Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.

Este método genera un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que se especifique **adCopyOverWrite**.

> [!IMPORTANT]
> Utilice la opción **adCopyOverWrite** con criterio. Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio, se *eliminará* el directorio y se reemplazará con el archivo.


> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Direcciones URL absolutas y relativas.](absolute-and-relative-urls.md)


