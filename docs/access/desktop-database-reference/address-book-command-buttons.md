---
title: Botones de comando de la libreta de direcciones
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282481"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="8fbf6-102">Botones de comando de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="8fbf6-102">Address Book command buttons</span></span>


<span data-ttu-id="8fbf6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fbf6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8fbf6-104">La aplicación Libreta de direcciones incluye los siguientes botones de comando:</span><span class="sxs-lookup"><span data-stu-id="8fbf6-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="8fbf6-105">Un botón **Buscar** para enviar una consulta a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="8fbf6-106">Un botón **Borrar** para borrar los cuadros de texto antes de iniciar una nueva búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="8fbf6-107">Un botón **Actualizar perfil** para guardar los cambios de un registro de empleado.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="8fbf6-108">Un botón **Cancelar cambios** para descartar cambios.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="8fbf6-109">Botón Buscar</span><span class="sxs-lookup"><span data-stu-id="8fbf6-109">Find Button</span></span>

<span data-ttu-id="8fbf6-110">Al hacer clic en el botón **Buscar** , se\_activa el procedimiento Sub OnClick de búsqueda de VBScript, que genera y envía la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="8fbf6-111">Al hacer clic en este botón, se rellena la cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="8fbf6-112">Generar la consulta SQL</span><span class="sxs-lookup"><span data-stu-id="8fbf6-112">Building the SQL Query</span></span>

<span data-ttu-id="8fbf6-113">La primera parte del procedimiento Find\_OnClick genera la consulta SQL, una frase cada vez, anexando cadenas de texto a una instrucción SQL SELECT global.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="8fbf6-114">Comienza estableciendo la variable en una instrucción SELECT de SQL que solicita todas las filas de datos de la tabla de origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="8fbf6-115">A continuación, el subprocedimiento examina cada uno de los cuatro cuadros de entrada de la página.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="8fbf6-116">Dado que el programa utiliza la palabra en la creación de instrucciones SQL, las consultas son búsquedas de subcadenas en lugar de coincidencias exactas.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="8fbf6-117">Por ejemplo, si el cuadro **Apellido** contenía la entrada "Berge" y el cuadro **title** contenía la entrada "Program Manager", la instrucción SQL (valor de) leería lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8fbf6-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="8fbf6-118">Si la consulta obtuvo resultados, todas las personas cuyo apellido contiene el texto "Berge" (tales como Berge y Berger) y cuyo título o cargo contiene las palabras "Program Manager" (por ejemplo, Program Manager, Advanced Technologies) aparecerán en la cuadrícula de datos HTML.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="8fbf6-119">Preparar y enviar la consulta</span><span class="sxs-lookup"><span data-stu-id="8fbf6-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="8fbf6-120">La última parte del procedimiento de\_la cláusula Find OnClick consta de dos instrucciones.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="8fbf6-121">La primera instrucción asigna a la propiedad SQL del objeto RDS.DataControl la consulta SQL generada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="8fbf6-122">La segunda instrucción hace que el **objeto RDS. DataControl** () para consultar la base de datos y, a continuación, mostrar los nuevos resultados de la consulta en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="8fbf6-123">Botón Actualizar perfil</span><span class="sxs-lookup"><span data-stu-id="8fbf6-123">Update Profile Button</span></span>

<span data-ttu-id="8fbf6-124">Al hacer clic en el botón **Actualizar perfil** , se\_activa el procedimiento Sub de VBScript Update OnClick, que ejecuta el objeto RDS. DataControl () los métodos SubmitChanges y Refresh.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="8fbf6-125">Cuando DC1. SubmitChanges se ejecuta, el servicio de datos remotos empaqueta toda la información de actualización y la envía al servidor mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="8fbf6-126">La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="8fbf6-127">, el servicio de datos remotos (RDS) empaqueta toda la información de actualización y la envía al servidor mediante HTTP.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="8fbf6-128">La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="8fbf6-129">DC1. Refresh no es necesario después de **SubmitChanges** con el servicio de datos remoto, pero garantiza datos actualizados.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="8fbf6-130">Botón Cancelar cambios</span><span class="sxs-lookup"><span data-stu-id="8fbf6-130">Cancel Changes Button</span></span>

<span data-ttu-id="8fbf6-131">Al hacer clic en **Cancelar cambios** , se\_activa el procedimiento Sub OnClick de VBScript, que ejecuta el objeto RDS. DataControl (método CancelUpdate).</span><span class="sxs-lookup"><span data-stu-id="8fbf6-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="8fbf6-132">Cuando se ejecuta, descarta cualquier modificación que haya realizado un usuario en un registro de empleado en la cuadrícula de datos desde la última consulta o actualización.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="8fbf6-133">Restaura los valores originales.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-133">It restores the original values.</span></span>

