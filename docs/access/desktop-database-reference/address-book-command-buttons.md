---
title: Botones de comando de la Libreta de direcciones
TOCTitle: Address Book Command Buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e445414ead78bb5e1b05b3f3812e86f1d6c119ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869515"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="67755-102">Botones de comando de la Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="67755-102">Address Book Command Buttons</span></span>


<span data-ttu-id="67755-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67755-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="67755-104">La aplicación Libreta de direcciones incluye los siguientes botones de comando:</span><span class="sxs-lookup"><span data-stu-id="67755-104">The Address Book application includes the following command buttons:</span></span>

  - <span data-ttu-id="67755-105">Un botón Buscar para enviar una consulta a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="67755-105">A Find button to submit a query to the database.</span></span>

  - <span data-ttu-id="67755-106">Un botón **Borrar** para borrar los cuadros de texto antes de iniciar una nueva búsqueda.</span><span class="sxs-lookup"><span data-stu-id="67755-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

  - <span data-ttu-id="67755-107">Un botón Actualizar perfil para guardar los cambios de un registro de empleado.</span><span class="sxs-lookup"><span data-stu-id="67755-107">An Update Profile button to save changes to an employee record.</span></span>

  - <span data-ttu-id="67755-108">Un botón Cancelar cambios para descartar cambios.</span><span class="sxs-lookup"><span data-stu-id="67755-108">A Cancel Changes button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="67755-109">Botón Buscar</span><span class="sxs-lookup"><span data-stu-id="67755-109">Find Button</span></span>

<span data-ttu-id="67755-110">Al hacer clic en el botón **Buscar** , se activa la búsqueda de VBScript\_procedimiento OnClick Sub, que genera y envía la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="67755-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="67755-111">Al hacer clic en este botón, se rellena la cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="67755-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="67755-112">Generar la consulta SQL</span><span class="sxs-lookup"><span data-stu-id="67755-112">Building the SQL Query</span></span>

<span data-ttu-id="67755-113">La primera parte de la búsqueda\_procedimiento OnClick Sub basa la consulta SQL, una frase a la vez, anexando cadenas de texto a una instrucción SELECT de SQL global.</span><span class="sxs-lookup"><span data-stu-id="67755-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="67755-114">Comienza estableciendo la variable en una instrucción SELECT de SQL que solicita todas las filas de datos de la tabla de origen de datos.</span><span class="sxs-lookup"><span data-stu-id="67755-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="67755-115">A continuación, el subprocedimiento examina cada uno de los cuatro cuadros de entrada de la página.</span><span class="sxs-lookup"><span data-stu-id="67755-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="67755-116">Dado que el programa utiliza la palabra en la creación de las instrucciones SQL, las consultas son búsquedas de subcadenas, en vez de coincidencias exactas.</span><span class="sxs-lookup"><span data-stu-id="67755-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="67755-117">Por ejemplo, si **el cuadro** LastName contenía la entrada "Berge" y el cuadro **Title** la entrada "Program Manager", la instrucción SQL (valor) será:</span><span class="sxs-lookup"><span data-stu-id="67755-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="67755-118">Si la consulta obtuvo resultados, todas las personas cuyo apellido contiene el texto "Berge" (tales como Berge y Berger) y cuyo título o cargo contiene las palabras "Program Manager" (por ejemplo, Program Manager, Advanced Technologies) aparecerán en la cuadrícula de datos HTML.</span><span class="sxs-lookup"><span data-stu-id="67755-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="67755-119">Preparar y enviar la consulta</span><span class="sxs-lookup"><span data-stu-id="67755-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="67755-120">La última parte de la búsqueda\_procedimiento OnClick Sub consta de dos instrucciones.</span><span class="sxs-lookup"><span data-stu-id="67755-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="67755-121">La primera instrucción asigna a la propiedad SQL del objeto RDS.DataControl la consulta SQL generada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="67755-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="67755-122">La segunda instrucción hace que el **RDS. DataControl** () para consultar la base de datos de objetos y, a continuación, muestre los nuevos resultados de la consulta en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="67755-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="67755-123">Botón Actualizar perfil</span><span class="sxs-lookup"><span data-stu-id="67755-123">Update Profile Button</span></span>

<span data-ttu-id="67755-124">Al hacer clic en el botón **Actualizar perfil** , se activa la actualización de VBScript\_procedimiento OnClick Sub, que se ejecuta el objeto RDS. Métodos de SubmitChanges y Refresh de () del objeto DataControl.</span><span class="sxs-lookup"><span data-stu-id="67755-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="67755-125">Cuando DC1. Ejecuta SubmitChanges, el servicio de datos remoto empaqueta toda la información de actualización y se envía al servidor a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="67755-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="67755-126">La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="67755-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="67755-127">, el servicio de datos remotos (RDS) empaqueta toda la información de actualización y la envía al servidor mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="67755-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="67755-128">La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="67755-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="67755-129">DC1. Refresh no es necesario después de **SubmitChanges** con RDS, pero garantiza datos actualizados.</span><span class="sxs-lookup"><span data-stu-id="67755-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="67755-130">Botón Cancelar cambios</span><span class="sxs-lookup"><span data-stu-id="67755-130">Cancel Changes Button</span></span>

<span data-ttu-id="67755-131">Al hacer clic en **Cancelar cambios** , se activa la cancelación de VBScript\_procedimiento OnClick Sub, que se ejecuta el objeto RDS. Del objeto DataControl (método CancelUpdate.</span><span class="sxs-lookup"><span data-stu-id="67755-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="67755-132">Cuando se ejecuta, éste descarta cualquier modificación que ha realizado un usuario en un registro de empleado en la cuadrícula de datos desde la última consulta o actualización.</span><span class="sxs-lookup"><span data-stu-id="67755-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="67755-133">Restaura los valores originales.</span><span class="sxs-lookup"><span data-stu-id="67755-133">It restores the original values.</span></span>

