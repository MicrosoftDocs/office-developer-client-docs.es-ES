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
# <a name="appendchunk-method-ado"></a><span data-ttu-id="253c3-102">AppendChunk (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="253c3-102">AppendChunk method (ADO)</span></span>


<span data-ttu-id="253c3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="253c3-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="253c3-104">Anexa datos a un objeto [Field](field-object-ado.md) de texto o de datos binarios de gran tamaño, o bien, a un objeto [Parameter](parameter-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="253c3-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="253c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="253c3-105">Syntax</span></span>

<span data-ttu-id="253c3-106">*objeto.* AppendChunk *datos*</span><span class="sxs-lookup"><span data-stu-id="253c3-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="253c3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="253c3-107">Parameters</span></span>

  - <span data-ttu-id="253c3-108">*objeto*</span><span class="sxs-lookup"><span data-stu-id="253c3-108">*object*</span></span>

  - <span data-ttu-id="253c3-109">Objeto **Field** o **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="253c3-109">A **Field** or **Parameter** object.</span></span>

  - <span data-ttu-id="253c3-110">*Datos*</span><span class="sxs-lookup"><span data-stu-id="253c3-110">*Data*</span></span>

  - <span data-ttu-id="253c3-111">**Variant** que contiene los datos que se van a anexar al objeto.</span><span class="sxs-lookup"><span data-stu-id="253c3-111">A **Variant** that contains the data to append to the object.</span></span>

## <a name="remarks"></a><span data-ttu-id="253c3-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="253c3-112">Remarks</span></span>

<span data-ttu-id="253c3-p101">Utilice el método **AppendChunk** en un objeto **Field** o **Parameter** para rellenarlo con datos binarios o de caracteres de gran tamaño. En los casos en los que la memoria del sistema está limitada, puede usar el método **AppendChunk** para manipular los valores largos en diferentes partes en lugar de manipularlos en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="253c3-p101">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data. In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="253c3-115">**Field**</span><span class="sxs-lookup"><span data-stu-id="253c3-115">**Field**</span></span>

<span data-ttu-id="253c3-116">Si el valor del bit **adFldLong** en la propiedad [Attributes](attributes-property-ado.md) de un objeto **Field** está establecido en true, puede usar el método **AppendChunk** para ese campo.</span><span class="sxs-lookup"><span data-stu-id="253c3-116">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="253c3-p102">La primera llamada a **AppendChunk** en un objeto **Field** escribe los datos en el campo, sobrescribiendo todos los datos existentes. Las llamadas posteriores a **AppendChunk** agregan los datos a los datos existentes. Si anexa datos a un campo y, a continuación, establece o lee el valor de otro campo del registro actual, ADO supone que ha terminado de anexar datos al primer campo. Si llama de nuevo al método **AppendChunk** en el primer campo, ADO interpreta la llamada como una nueva operación de **AppendChunk** y sobrescribe los datos existentes. Si se obtiene acceso a los campos de otros objetos [Recordset](recordset-object-ado.md) que no sean copias del primer objeto **Recordset**, no se interrumpirán las operaciones de **AppendChunk**.</span><span class="sxs-lookup"><span data-stu-id="253c3-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="253c3-122">Si no hay un registro actual cuando llama a **AppendChunk** en un objeto **Field**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="253c3-122">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="253c3-p103">[!NOTA] El método **AppendChunk** no se ejecuta en los objetos **Field** de un objeto [Record](record-object-ado.md). No realiza ninguna operación y producirá un error de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="253c3-p103">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>



<span data-ttu-id="253c3-125">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="253c3-125">**Parameter**</span></span>

<span data-ttu-id="253c3-126">Si el valor del bit **adParamLong** en la propiedad **Attributes** de un objeto **Parameter** está establecido en true, puede utilizar el método **AppendChunk** para ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="253c3-126">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="253c3-p104">La primera llamada a **AppendChunk** en un objeto **Parameter** escribe los datos en el parámetro, sobrescribiendo los datos existentes. Las llamadas posteriores a **AppendChunk** en un objeto **Parameter** agregan los datos a los datos de parámetro existentes. Una llamada a **AppendChunk** que pasa un valor null descarta todos los datos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="253c3-p104">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data. Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data. An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>

