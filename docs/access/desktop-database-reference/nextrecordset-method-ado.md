---
title: NextRecordset (método, ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b824dc1b00f913e097432aae65ecac425ef19031
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486617"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="5fcb5-102">NextRecordset (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="5fcb5-102">NextRecordset Method (ADO)</span></span>


<span data-ttu-id="5fcb5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fcb5-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="5fcb5-104">Borra el objeto [Recordset](recordset-object-ado.md) actual y devuelve el siguiente objeto **Recordset** recorriendo varios comandos.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fcb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fcb5-105">Syntax</span></span>

<span data-ttu-id="5fcb5-106">Establecer *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="5fcb5-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="5fcb5-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fcb5-107">Return Value</span></span>

<span data-ttu-id="5fcb5-p101">Devuelve un objeto **Recordset**. En el modelo de sintaxis, \* recordset1\* y *recordset2* pueden ser el mismo objeto **Recordset**, o bien, pueden ser objetos independientes. Si utiliza objetos **Recordset** independientes y restablece el valor de la propiedad **ActiveConnection** en el objeto **Recordset** original (*recordset1*), se generará un error después de llamar a **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fcb5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fcb5-111">Parameters</span></span>

- <span data-ttu-id="5fcb5-112">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="5fcb5-112">*RecordsAffected*</span></span>

- <span data-ttu-id="5fcb5-p102">Es opcional. Variable de tipo **Long** a la que el proveedor devuelve el número de registros afectados por la actual operación.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5fcb5-115">[!NOTA] Este parámetro sólo devuelve el número de registros que se ven afectados por una operación; no devuelve un número de registros de una instrucción SELECT usada para generar el objeto <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-115">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <STRONG>Recordset</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="5fcb5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fcb5-116">Remarks</span></span>

<span data-ttu-id="5fcb5-117">Utilice el método **NextRecordset** para devolver los resultados del siguiente comando en una instrucción de comando compuesta o de un procedimiento almacenado que devuelve varios resultados.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-117">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="5fcb5-118">Si abre un objeto **Recordset** basado en una instrucción de comando compuesta (por ejemplo, "seleccione \* FROM Tabla1; Seleccione \* FROM Tabla2 ") mediante el método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) en un [comando](command-object-ado.md) o el método [Open](open-method-ado-recordset.md) en un **objeto Recordset**, ADO ejecuta sólo el primer comando y devuelve los resultados al *objeto recordset*.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-118">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="5fcb5-119">Para obtener acceso a los resultados de los comandos subsiguientes de la instrucción, llame al método **NextRecordset** .</span><span class="sxs-lookup"><span data-stu-id="5fcb5-119">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="5fcb5-120">Mientras haya resultados adicionales y el objeto **Recordset** que contiene las instrucciones compuestas no esté desconectado ni se hayan calculado las referencias de los límites del proceso, el método **NextRecordset** seguirá devolviendo objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-120">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="5fcb5-121">Si un comando que devuelve filas se ejecuta correctamente pero no devuelve registros, el objeto **Recordset** devuelto estará abierto pero vacío.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-121">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="5fcb5-122">Para ver si este es el caso, compruebe si el valor de las propiedades [BOF](bof-eof-properties-ado.md) y [EOF](bof-eof-properties-ado.md) es **True**.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-122">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="5fcb5-123">Si un comando no devuelve filas se ejecuta correctamente, el objeto **Recordset** devuelto estará cerrado, lo que puede comprobarse mediante la propiedad [State](state-property-ado.md) en el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-123">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="5fcb5-124">Cuando no hay ningún resultado más, *recordset* se establecerá en *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-124">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="5fcb5-125">El método **NextRecordset** no está disponible en un objeto **Recordset** desconectado, donde el valor de [ActiveConnection](activeconnection-property-ado.md) es **Nothing** (en Microsoft Visual Basic) o NULL (en otros lenguajes).</span><span class="sxs-lookup"><span data-stu-id="5fcb5-125">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="5fcb5-126">Si hay una modificación en curso mientras se está en modo de actualización inmediata y se llama al método **NextRecordset**, se generará un error; llame primero al método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5fcb5-126">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="5fcb5-p105">Para pasar parámetros para más de un comando en la instrucción compuesta rellenando la colección [Parameters](parameters-collection-ado.md), o bien, pasando una matriz con la llamada original a **Abrir** o **Execute**, los parámetros deben estar en el mismo orden en la colección o matriz que sus respectivos comandos en la serie de comandos. Es preciso terminar de leer todos los resultados antes de leer los valores de los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="5fcb5-p106">El proveedor OLE DB determina cuándo se ejecuta cada comando de una instrucción compuesta. Por ejemplo, el [proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md) ejecuta todos los comandos de un lote después de recibir la instrucción compuesta. Los objetos **Recordset** resultantes se devuelven simplemente al llamar a **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="5fcb5-p107">Sin embargo, puede que otros proveedores ejecuten el siguiente comando de una instrucción sólo después de una llamada a NextRecordset. En este caso, si cierra explícitamente el objeto **Recordset** antes de ejecutar paso a paso toda la instrucción de comandos, ADO no ejecutará nunca los comandos restantes.</span><span class="sxs-lookup"><span data-stu-id="5fcb5-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>

