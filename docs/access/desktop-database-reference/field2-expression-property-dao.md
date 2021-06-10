---
title: Propiedad Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292821"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="ea5e8-102">Propiedad Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="ea5e8-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="ea5e8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea5e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea5e8-104">Obtiene o establece una expresión que representa la fórmula de un campo calculado.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="ea5e8-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="ea5e8-106">Información de versión</span><span class="sxs-lookup"><span data-stu-id="ea5e8-106">Version information</span></span>

<span data-ttu-id="ea5e8-107">Versión agregada: Access 2010</span><span class="sxs-lookup"><span data-stu-id="ea5e8-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="ea5e8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea5e8-108">Syntax</span></span>

<span data-ttu-id="ea5e8-109">*expresión* . Expresión</span><span class="sxs-lookup"><span data-stu-id="ea5e8-109">*expression* .Expression</span></span>

<span data-ttu-id="ea5e8-110">*expression* Variable que representa un objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea5e8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea5e8-111">Remarks</span></span>

<span data-ttu-id="ea5e8-112">En Access 2013, puede crear campos de tabla que calcule valores.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="ea5e8-113">Los cálculos pueden incluir valores de campos de la misma tabla, así como funciones integradas de Access.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="ea5e8-114">El cálculo no puede incluir campos de otras tablas o consultas.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="ea5e8-115">Los resultados del cálculo son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="ea5e8-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea5e8-116">Example</span></span>

<span data-ttu-id="ea5e8-p103">En el siguiente ejemplo, se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="ea5e8-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="ea5e8-120">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ea5e8-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

