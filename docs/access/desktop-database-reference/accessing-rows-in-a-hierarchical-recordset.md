---
<span data-ttu-id="eb4a5-101"><<<<<<< Título HEAD: obtener acceso a filas en una TOCTitle de conjunto de registros jerárquico: acceso a filas de un objeto Recordset jerárquico ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 09/18 / 2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="eb4a5-101"><<<<<<< HEAD title: Accessing Rows in a Hierarchical Recordset TOCTitle: Accessing Rows in a Hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="eb4a5-102">Obtener acceso a las filas de un objeto Recordset jerárquico</span><span class="sxs-lookup"><span data-stu-id="eb4a5-102">Accessing Rows in a Hierarchical Recordset</span></span>

<span data-ttu-id="eb4a5-103">=== título: obtener acceso a las filas de un Recordset TOCTitle jerárquico: obtener acceso a las filas de un ms:assetid de conjunto de registros jerárquico: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 17/10/2018 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="eb4a5-103">======= title: Accessing rows in a hierarchical Recordset TOCTitle: Accessing rows in a hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="eb4a5-104">Acceso a las filas de un Recordset jerárquico</span><span class="sxs-lookup"><span data-stu-id="eb4a5-104">Accessing rows in a hierarchical Recordset</span></span>
>>>>>>> <span data-ttu-id="eb4a5-105">master</span><span class="sxs-lookup"><span data-stu-id="eb4a5-105">master</span></span>

<span data-ttu-id="eb4a5-106">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb4a5-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb4a5-107">En el ejemplo siguiente, se muestran los pasos necesarios para obtener acceso a filas de un objeto [Recordset](recordset-object-ado.md) jerárquico:</span><span class="sxs-lookup"><span data-stu-id="eb4a5-107">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

<span data-ttu-id="eb4a5-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="eb4a5-108"><<<<<<< HEAD</span></span>
1.  <span data-ttu-id="eb4a5-109">Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-109">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="eb4a5-110">El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-110">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="eb4a5-111">El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-111">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="eb4a5-112">El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-112">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a><span data-ttu-id="eb4a5-113">(La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE (falso) como ejemplo, de modo que se pueda ver el cambio de capítulo explícitamente en cada iteración del bucle externo.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-113">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="eb4a5-114">Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-114">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="eb4a5-115">A continuación, establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.)</span><span class="sxs-lookup"><span data-stu-id="eb4a5-115">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>
=======
1. <span data-ttu-id="eb4a5-116">Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-116">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="eb4a5-117">El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-117">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="eb4a5-118">El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-118">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="eb4a5-119">El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-119">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="eb4a5-120">La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE para fines de ilustración, para que pueda ver el capítulo cambiar explícitamente en cada iteración del bucle externo.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-120">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="eb4a5-121">Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-121">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="eb4a5-122">Establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.</span><span class="sxs-lookup"><span data-stu-id="eb4a5-122">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>
>>>>>>> <span data-ttu-id="eb4a5-123">master</span><span class="sxs-lookup"><span data-stu-id="eb4a5-123">master</span></span>

<span data-ttu-id="eb4a5-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="eb4a5-124">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

