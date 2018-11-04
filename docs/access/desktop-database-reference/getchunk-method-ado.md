---
title: GetChunk (método, ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27d6f2c9884441042d67615072738c7762f4f789
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949918"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="4b007-102">GetChunk (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="4b007-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="4b007-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b007-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b007-104">Devuelve todo o parte del contenido de un objeto [Field](field-object-ado.md) de datos binarios o de texto de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="4b007-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b007-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b007-105">Syntax</span></span>

<span data-ttu-id="4b007-106">*variable* = *campo*. GetChunk (*tamaño* )</span><span class="sxs-lookup"><span data-stu-id="4b007-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="4b007-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b007-107">Return value</span></span>

<span data-ttu-id="4b007-108">Devuelve un valor de tipo **Variant**.</span><span class="sxs-lookup"><span data-stu-id="4b007-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b007-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b007-109">Parameters</span></span>

|<span data-ttu-id="4b007-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4b007-110">Parameter</span></span>|<span data-ttu-id="4b007-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b007-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4b007-112">*Size*</span><span class="sxs-lookup"><span data-stu-id="4b007-112">*Size*</span></span> |<span data-ttu-id="4b007-113">Expresión de tipo **Long** que equivale al número de bytes o caracteres que se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="4b007-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4b007-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b007-114">Remarks</span></span>

<span data-ttu-id="4b007-p101">Utilice el método **GetChunk** en un objeto **Field** para recuperar todo o parte de sus datos binarios o de caracteres de gran tamaño. En los casos en los que la memoria del sistema está limitada, puede usar el método **GetChunk** para manipular los valores largos en diversas partes en lugar de manipularlos en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="4b007-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="4b007-p102">Los datos devueltos por una llamada a **GetChunk** se asignan a *variable*. Si el valor de *Size* es mayor que el de los datos restantes, el método **GetChunk** devuelve sólo los datos restantes sin rellenar *variable* con espacios en blanco. Si el campo está vacío, el método **GetChunk** devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="4b007-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="4b007-p103">Cada llamada subsiguiente a **GetChunk** recupera datos a partir de la ubicación donde finalizó la anterior llamada a **GetChunk**. Sin embargo, si está recuperando datos de un campo y, a continuación, establece o lee el valor de otro campo del actual registro, ADO supone que ha terminado de recuperar los datos del primer campo. Si vuelve a llamar al método **GetChunk** en el primer campo, ADO interpreta la llamada como una nueva operación de **GetChunk** e inicia la lectura desde el principio de los datos. Si obtiene acceso a los campos de otros objetos [Recordset](recordset-object-ado.md) que no sean copias del primer objeto **Recordset**, no se interrumpirán las operaciones de **GetChunk**.</span><span class="sxs-lookup"><span data-stu-id="4b007-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="4b007-124">Si el valor del bit **adFldLong** en la propiedad [Attributes](attributes-property-ado.md) de un objeto **Field** está establecido en **True**, puede usar el método **GetChunk** para ese campo.</span><span class="sxs-lookup"><span data-stu-id="4b007-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="4b007-125">Si no hay ningún registro actual cuando utiliza el método **GetChunk** en un objeto **Field**, se producirá el error 3021 (No hay registro actual).</span><span class="sxs-lookup"><span data-stu-id="4b007-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="4b007-p104">[!NOTA] El método **GetChunk** no se ejecuta en los objetos **Field** de un objeto [Record](record-object-ado.md). No realiza ninguna operación y generará un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4b007-p104">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>


