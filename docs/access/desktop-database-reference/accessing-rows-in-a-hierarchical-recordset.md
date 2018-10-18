---
<<<<<<< Título HEAD: obtener acceso a filas en una TOCTitle de conjunto de registros jerárquico: acceso a filas de un objeto Recordset jerárquico ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 09/18 / 2015 mtps_version: Office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Obtener acceso a las filas de un objeto Recordset jerárquico

=== título: obtener acceso a las filas de un Recordset TOCTitle jerárquico: obtener acceso a las filas de un ms:assetid de conjunto de registros jerárquico: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 17/10/2018 mtps_version: v = Office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Acceso a las filas de un Recordset jerárquico
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

En el ejemplo siguiente, se muestran los pasos necesarios para obtener acceso a filas de un objeto [Recordset](recordset-object-ado.md) jerárquico:

<<<<<<< HEAD
1.  Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.

2.  El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.

3.  El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.

4.  El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a>(La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE (falso) como ejemplo, de modo que se pueda ver el cambio de capítulo explícitamente en cada iteración del bucle externo. Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez. A continuación, establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.)
=======
1. Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.

2. El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.

3. El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.

4. El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.

> [!NOTE] 
> La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE para fines de ilustración, para que pueda ver el capítulo cambiar explícitamente en cada iteración del bucle externo. Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez. Establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.
>>>>>>> master

**Ejemplo**

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

