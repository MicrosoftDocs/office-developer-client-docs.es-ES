---
<span data-ttu-id="6fcd4-101"><<<<<<< Título HEAD: SQLState (propiedad) (ADO) TOCTitle: SQLState (propiedad) (ADO) === título: SQLState (propiedad, ADO) TOCTitle: SQLState (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6fcd4-101"><<<<<<< HEAD title: SQLState Property (ADO) TOCTitle: SQLState Property (ADO) ======= title: SQLState property (ADO) TOCTitle: SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6fcd4-102">Master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: ms.date 48547806: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="6fcd4-102">master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6fcd4-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6fcd4-103"><<<<<<< HEAD</span></span>
# <a name="sqlstate-property-ado"></a><span data-ttu-id="6fcd4-104">SQLState (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6fcd4-104">SQLState Property (ADO)</span></span>
=======
# <a name="sqlstate-property-ado"></a><span data-ttu-id="6fcd4-105">SQLState (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6fcd4-105">SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6fcd4-106">master</span><span class="sxs-lookup"><span data-stu-id="6fcd4-106">master</span></span>


<span data-ttu-id="6fcd4-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fcd4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6fcd4-108">Indica el estado SQL de un objeto [Error](error-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-108">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="6fcd4-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6fcd4-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6fcd4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fcd4-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6fcd4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fcd4-111">Return value</span></span>
>>>>>>> <span data-ttu-id="6fcd4-112">master</span><span class="sxs-lookup"><span data-stu-id="6fcd4-112">master</span></span>

<span data-ttu-id="6fcd4-113">Devuelve un valor de cinco caracteres de tipo **String** que sigue el estándar ANSI SQL e indica el código del error.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-113">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcd4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6fcd4-114">Remarks</span></span>

<span data-ttu-id="6fcd4-p101">Use la propiedad **SQLState** para leer el código de error de cinco caracteres que devuelve el proveedor cuando se produce un error durante el procesamiento de una instrucción SQL. Por ejemplo, cuando se usa el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error de estado SQL se originan en ODBC, basándose en errores específicos de ODBC o en errores que se originan en Microsoft SQL Server, y se asignan a errores ODBC. Estos códigos de error están documentados en el estándar ANSI de SQL, pero pueden ser implementados de formas diferentes por los distintos orígenes de datos.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

