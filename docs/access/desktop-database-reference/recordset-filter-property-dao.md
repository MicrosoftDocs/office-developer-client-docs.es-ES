---
title: Propiedad Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ae33c9b7979e6dd98d94652a61c8737397c7a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884306"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="6b1f6-102">Propiedad Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b1f6-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="6b1f6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b1f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b1f6-p101">Establece o devuelve un valor que determina los registros incluidos en un objeto **Recordset** abierto posteriormente (solo en áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b1f6-106">Syntax</span></span>

<span data-ttu-id="6b1f6-107">*expresión* . Filtro</span><span class="sxs-lookup"><span data-stu-id="6b1f6-107">*expression* .Filter</span></span>

<span data-ttu-id="6b1f6-108">*expresión* Expresión que devuelve un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="6b1f6-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1f6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b1f6-109">Remarks</span></span>

<span data-ttu-id="6b1f6-110">La configuración o el valor devuelto es un tipo de datos String que contiene la cláusula WHERE de una instrucción SQL sin la palabra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="6b1f6-111">Utilice la propiedad **Filter** para aplicar un filtro a un dynaset, instantánea u objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="6b1f6-112">Puede usar la propiedad **Filter** para limitar los registros que se devuelven desde un objeto existente cuando un nuevo objeto **Recordset** se abre basado en un objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="6b1f6-113">Utilice el formato de fecha de Estados Unidos (mes-día-año) cuando filtre campos que contengan fechas, incluso si no utiliza la versión de Estados Unidos del motor de base de datos de Microsoft Access (en cuyo caso debe reunir cualquier fecha concatenando cadenas, por ejemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="6b1f6-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="6b1f6-114">De lo contrario, puede que no se filtren los datos de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="6b1f6-115">En mucho casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="6b1f6-116">Si establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strFilter = "PRICE \> " & lngPrice y lngPrice = 125,50), se produce un error al intentar Abra el siguiente **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="6b1f6-117">Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y Microsoft Access SQL sólo acepta caracteres decimales anglosajones.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="6b1f6-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b1f6-118">Example</span></span>

<span data-ttu-id="6b1f6-119">En el siguiente ejemplo se muestra cómo usar la propiedad Filter para determinar los registros que se incluirán en un Recordset que se abrirá a continuación.</span><span class="sxs-lookup"><span data-stu-id="6b1f6-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="6b1f6-120">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6b1f6-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
