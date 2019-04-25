---
title: Propiedad Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 7ab090dd6cf0b6e2676cf05907ac77c438f22652
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284823"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="ad62d-102">Propiedad Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad62d-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="ad62d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad62d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad62d-104">Establece o devuelve un valor que determina los registros incluidos en un objeto **Recordset** abierto posteriormente (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ad62d-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="ad62d-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ad62d-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad62d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad62d-106">Syntax</span></span>

<span data-ttu-id="ad62d-107">*expression* .Filter</span><span class="sxs-lookup"><span data-stu-id="ad62d-107">expression  . Filter</span></span>

<span data-ttu-id="ad62d-108">*expression* Expresión que devuelve un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ad62d-108">*expression*  An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad62d-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad62d-109">Remarks</span></span>

<span data-ttu-id="ad62d-110">La configuración o el valor devuelto es un tipo de datos String que contiene la cláusula WHERE de una instrucción SQL sin la palabra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="ad62d-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="ad62d-111">Use la propiedad **Filter** para aplicar un filtro a un objeto **Recordset** de tipo Dynaset, Snapshot o solo avance.</span><span class="sxs-lookup"><span data-stu-id="ad62d-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="ad62d-112">Puede usar la propiedad **Filter** para limitar los registros que se devuelven desde un objeto existente cuando un nuevo objeto **Recordset** se abre basado en un objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="ad62d-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="ad62d-113">Utilice el formato de fecha de Estados Unidos (mes-día-año) cuando filtre campos que contengan fechas, incluso si no está utilizando una versión de Estados Unidos del motor de base de datos Microsoft Access (en cuyo caso debe reunir cualquier fecha concatenando cadenas, por ejemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="ad62d-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="ad62d-114">De lo contrario, puede que no se filtren los datos de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="ad62d-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="ad62d-115">En mucho casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ad62d-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="ad62d-116">Si configura la propiedad en una cadena concatenada con un valor no entero y los parámetros del sistema especifican un carácter decimal distinto del estándar de Estados Unidos, como una coma (por ejemplo, strFilter = "PRICE \> " & lngPrice y lngPrice = 125,50), aparecerá un error cuando intente abrir el siguiente objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ad62d-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next Recordset.</span></span> <span data-ttu-id="ad62d-117">Esto se produce porque durante la concatenación, el número se convertirá en una cadena usando el carácter decimal predeterminado del sistema y Microsoft Access SQL solo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="ad62d-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="ad62d-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad62d-118">Example</span></span>

<span data-ttu-id="ad62d-119">En el siguiente ejemplo se muestra cómo usar la propiedad Filter para determinar los registros que se incluirán en un Recordset que se abrirá posteriormente.</span><span class="sxs-lookup"><span data-stu-id="ad62d-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="ad62d-120">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ad62d-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
