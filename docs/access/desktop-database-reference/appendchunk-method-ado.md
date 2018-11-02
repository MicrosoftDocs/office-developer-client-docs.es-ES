---
title: AppendChunk (método, ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29af4adf95eeb47be18bd8cb8368c47fc0e70a85
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928267"
---
# <a name="appendchunk-method-ado"></a>AppendChunk (método, ADO)


**Se aplica a**: Access 2013, Office 2013


Anexa datos a un objeto [Field](field-object-ado.md) de texto o de datos binarios de gran tamaño, o bien, a un objeto [Parameter](parameter-object-ado.md).

## <a name="syntax"></a>Sintaxis

*objeto.* AppendChunk *datos*

## <a name="parameters"></a>Parámetros

  - *objeto*

  - Objeto **Field** o **Parameter**.

  - *Datos*

  - **Variant** que contiene los datos que se van a anexar al objeto.

## <a name="remarks"></a>Comentarios

Utilice el método **AppendChunk** en un objeto **Field** o **Parameter** para rellenarlo con datos binarios o de caracteres de gran tamaño. En los casos en los que la memoria del sistema está limitada, puede usar el método **AppendChunk** para manipular los valores largos en diferentes partes en lugar de manipularlos en su totalidad.

**Field**

Si el valor del bit **adFldLong** en la propiedad [Attributes](attributes-property-ado.md) de un objeto **Field** está establecido en true, puede usar el método **AppendChunk** para ese campo.

La primera llamada a **AppendChunk** en un objeto **Field** escribe los datos en el campo, sobrescribiendo todos los datos existentes. Las llamadas posteriores a **AppendChunk** agregan los datos a los datos existentes. Si anexa datos a un campo y, a continuación, establece o lee el valor de otro campo del registro actual, ADO supone que ha terminado de anexar datos al primer campo. Si llama de nuevo al método **AppendChunk** en el primer campo, ADO interpreta la llamada como una nueva operación de **AppendChunk** y sobrescribe los datos existentes. Si se obtiene acceso a los campos de otros objetos [Recordset](recordset-object-ado.md) que no sean copias del primer objeto **Recordset**, no se interrumpirán las operaciones de **AppendChunk**.

Si no hay un registro actual cuando llama a **AppendChunk** en un objeto **Field**, se produce un error.


> [!NOTE]
> [!NOTA] El método **AppendChunk** no se ejecuta en los objetos **Field** de un objeto [Record](record-object-ado.md). No realiza ninguna operación y producirá un error de tiempo de ejecución.



**Parámetro**

Si el valor del bit **adParamLong** en la propiedad **Attributes** de un objeto **Parameter** está establecido en true, puede utilizar el método **AppendChunk** para ese parámetro.

La primera llamada a **AppendChunk** en un objeto **Parameter** escribe los datos en el parámetro, sobrescribiendo los datos existentes. Las llamadas posteriores a **AppendChunk** en un objeto **Parameter** agregan los datos a los datos de parámetro existentes. Una llamada a **AppendChunk** que pasa un valor null descarta todos los datos de parámetro.

