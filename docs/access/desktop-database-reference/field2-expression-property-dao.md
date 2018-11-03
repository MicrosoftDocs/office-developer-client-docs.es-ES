---
title: Propiedad Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5869c381c7b449502cc2d28de8eeb214bbfb03d0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928659"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="0f4b8-102">Propiedad Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f4b8-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="0f4b8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f4b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f4b8-104">Obtiene o establece una expresión que representa la fórmula para un campo calculado.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="0f4b8-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="0f4b8-106">Información de versión</span><span class="sxs-lookup"><span data-stu-id="0f4b8-106">Version Information</span></span>

<span data-ttu-id="0f4b8-107">Versión añadida: Access 2010
</span><span class="sxs-lookup"><span data-stu-id="0f4b8-107">Version Added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="0f4b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f4b8-108">Syntax</span></span>

<span data-ttu-id="0f4b8-109">*expresión* . Expresión</span><span class="sxs-lookup"><span data-stu-id="0f4b8-109">*expression* .Expression</span></span>

<span data-ttu-id="0f4b8-110">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="0f4b8-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f4b8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f4b8-111">Remarks</span></span>

<span data-ttu-id="0f4b8-112">En Access 2013, puede crear los campos de tabla que calculan valores.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="0f4b8-113">Los cálculos pueden incluir los valores de campos en la misma tabla, así como las funciones integradas de acceso.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="0f4b8-114">El cálculo no puede incluir campos de otras tablas o consultas.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="0f4b8-115">Los resultados del cálculo son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="0f4b8-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f4b8-116">Example</span></span>

<span data-ttu-id="0f4b8-p103">En el siguiente ejemplo se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="0f4b8-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="0f4b8-120">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0f4b8-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

