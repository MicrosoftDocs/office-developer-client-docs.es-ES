---
title: Método GetChunk (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292289"
---
# <a name="getchunk-method-ado"></a>Método GetChunk (ADO)

**Se aplica a:** Access 2013, Office 2013

Devuelve todo o parte del contenido de un objeto [Field](field-object-ado.md) de datos binarios o de texto de gran tamaño.

## <a name="syntax"></a>Sintaxis

*variable*  =  *campo*. GetChunk(*Size* )

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant**.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Size* |Expresión de tipo **Long** que equivale al número de bytes o caracteres que se desea recuperar.|

## <a name="remarks"></a>Comentarios

Utilice el método **GetChunk** en un objeto **Field** para recuperar todo o parte de sus datos binarios o de caracteres de gran tamaño. En los casos en los que la memoria del sistema está limitada, puede usar el método **GetChunk** para manipular los valores largos en diversas partes en lugar de manipularlos en su totalidad.

Los datos devueltos por una llamada a **GetChunk** se asignan a *variable*. Si el valor de *Size* es mayor que el de los datos restantes, el método **GetChunk** devuelve sólo los datos restantes sin rellenar *variable* con espacios en blanco. Si el campo está vacío, el método **GetChunk** devuelve un valor nulo.

Cada llamada subsiguiente a **GetChunk** recupera datos a partir de la ubicación donde finalizó la anterior llamada a **GetChunk**. Sin embargo, si está recuperando datos de un campo y, a continuación, establece o lee el valor de otro campo del actual registro, ADO supone que ha terminado de recuperar los datos del primer campo. Si vuelve a llamar al método **GetChunk** en el primer campo, ADO interpreta la llamada como una nueva operación de **GetChunk** e inicia la lectura desde el principio de los datos. Si obtiene acceso a los campos de otros objetos [Recordset](recordset-object-ado.md) que no sean copias del primer objeto **Recordset**, no se interrumpirán las operaciones de **GetChunk**.

Si el valor del bit **adFldLong** en la propiedad [Attributes](attributes-property-ado.md) de un objeto **Field** está establecido en **True**, puede usar el método **GetChunk** para ese campo.

Si no hay ningún registro actual cuando utiliza el método **GetChunk** en un objeto **Field**, se producirá el error 3021 (No hay registro actual).


> [!NOTE]
> [!NOTA] El método **GetChunk** no se ejecuta en los objetos **Field** de un objeto [Record](record-object-ado.md). No realiza ninguna operación y generará un error en tiempo de ejecución.


