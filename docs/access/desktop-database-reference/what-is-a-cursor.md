---
title: ¿Qué es un cursor?  (Referencia de escritorio de la base de datos de access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb9321434dc039527daa99f2b24abf83a4c3383e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484439"
---
# <a name="what-is-a-cursor"></a><span data-ttu-id="da60e-103">¿Qué es un cursor?</span><span class="sxs-lookup"><span data-stu-id="da60e-103">What is a Cursor?</span></span>


<span data-ttu-id="da60e-104">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da60e-104">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="da60e-p102">Las operaciones de una base de datos relacional actúan sobre un conjunto completo de filas. El conjunto de filas devuelto por una instrucción SELECT está formado por todas las filas que cumplen las condiciones de la cláusula WHERE de la instrucción. Este conjunto completo de filas devuelto por la instrucción se conoce como el conjunto de resultados. Las aplicaciones, especialmente aquéllas que son interactivas y funcionan conectadas en línea, no pueden trabajar siempre eficazmente con todo el conjunto de resultados como una unidad. Estas aplicaciones necesitan un mecanismo que trabaje cada vez con una fila o un bloque pequeño de filas. Los cursores son una extensión de los conjuntos de resultados que proporciona ese mecanismo.</span><span class="sxs-lookup"><span data-stu-id="da60e-p102">Operations in a relational database act on a complete set of rows. The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement. This complete set of rows returned by the statement is known as the result set. Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit. These applications need a mechanism to work with one row or a small block of rows at a time. Cursors are an extension to result sets that provide that mechanism.</span></span>

<span data-ttu-id="da60e-p103">Un cursor se implementa mediante una biblioteca de cursores. Una biblioteca de cursores es software, implementado a menudo como parte de un sistema de base de datos o de una API de acceso a datos, que se utiliza para administrar atributos de los datos devueltos desde un origen de datos (un conjunto de resultados). Estos atributos incluyen la administración de la concurrencia, la posición en el conjunto de resultados, el número de filas devueltas y si se puede o no avanzar y/o retroceder por el conjunto de resultados (capacidad de desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="da60e-p103">A cursor is implemented by a cursor library. A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set). These attributes include concurrency management, position in the result set, number of rows returned, and whether or not you can move forward and/or backward through the result set (scrollability).</span></span>

<span data-ttu-id="da60e-p104">Un cursor realiza un seguimiento de la posición en el conjunto de resultados y permite realizar varias operaciones fila por fila en un conjunto de resultados, con o sin retorno a la tabla original. Es decir, los cursores devuelven conceptualmente un conjunto de resultados basado en las tablas de las bases de datos. El cursor se denomina así porque indica la posición actual en el conjunto de resultados, al igual que el cursor de una pantalla indica la posición actual en la misma.</span><span class="sxs-lookup"><span data-stu-id="da60e-p104">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table. In other words, cursors conceptually return a result set based on tables within the databases. The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</span></span>

<span data-ttu-id="da60e-117">Es importante familiarizarse con el concepto de cursores antes de pasar a aprender los detalles de su uso en ADO.</span><span class="sxs-lookup"><span data-stu-id="da60e-117">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</span></span>

<span data-ttu-id="da60e-118">Mediante el uso de los cursores, puede:</span><span class="sxs-lookup"><span data-stu-id="da60e-118">Using cursors, you can:</span></span>

  - <span data-ttu-id="da60e-119">Especificar el posicionamiento del conjunto de resultados en filas específicas.</span><span class="sxs-lookup"><span data-stu-id="da60e-119">Specify positioning at specific rows in the result set.</span></span>

  - <span data-ttu-id="da60e-120">Recuperar una fila o un bloque de filas según la posición actual del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="da60e-120">Retrieve one row or a block of rows based on the current result set position.</span></span>

  - <span data-ttu-id="da60e-121">Modificar los datos de las filas de la posición actual del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="da60e-121">Modify data in the rows at the current position in the result set.</span></span>

  - <span data-ttu-id="da60e-122">Definir diferentes niveles de sensibilidad a los cambios en los datos realizados por otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="da60e-122">Define different levels of sensitivity to data changes made by other users.</span></span>

<span data-ttu-id="da60e-p105">Por ejemplo, considere una aplicación que muestra una lista de los productos disponibles para un posible comprador. El comprador se desplaza por la lista para ver los detalles de los productos y los precios y, finalmente, selecciona un producto para su adquisición. Se producen desplazamientos y selecciones adicionales para el resto de la lista. Sin embargo, en lo que respecta al comprador, los productos aparecen de uno en uno, aunque la aplicación utilice un cursor desplazable para examinar el conjunto de resultados hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="da60e-p105">For example, consider an application that displays a list of available products to a potential buyer. The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase. Additional scrolling and selection occurs for the remainder of the list. As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</span></span>

<span data-ttu-id="da60e-127">Los cursores se pueden utilizar de varias formas:</span><span class="sxs-lookup"><span data-stu-id="da60e-127">You can use cursors in a variety of ways:</span></span>

  - <span data-ttu-id="da60e-128">Con ninguna fila.</span><span class="sxs-lookup"><span data-stu-id="da60e-128">With no rows at all.</span></span>

  - <span data-ttu-id="da60e-129">Con alguna o todas las filas de una sola tabla.</span><span class="sxs-lookup"><span data-stu-id="da60e-129">With some or all of the rows in a single table.</span></span>

  - <span data-ttu-id="da60e-130">Con alguna o todas las filas de tablas unidas lógicamente.</span><span class="sxs-lookup"><span data-stu-id="da60e-130">With some or all of the rows from logically joined tables.</span></span>

  - <span data-ttu-id="da60e-131">Como de sólo lectura o actualizables en el nivel de cursor o de campo.</span><span class="sxs-lookup"><span data-stu-id="da60e-131">As read-only or updateable at the cursor or field level.</span></span>

  - <span data-ttu-id="da60e-132">Como de sólo avance o con desplazamiento completo.</span><span class="sxs-lookup"><span data-stu-id="da60e-132">As forward-only or fully scrollable.</span></span>

  - <span data-ttu-id="da60e-133">Con el conjunto de claves de cursor ubicado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="da60e-133">With the cursor keyset located on the server.</span></span>

  - <span data-ttu-id="da60e-134">Con sensibilidad a los cambios de tablas subyacentes ocasionados por otras aplicaciones (como pertenencia a grupos de usuarios, ordenación, inserciones, actualizaciones y eliminaciones).</span><span class="sxs-lookup"><span data-stu-id="da60e-134">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</span></span>

  - <span data-ttu-id="da60e-135">Con presencia en el servidor o en el cliente.</span><span class="sxs-lookup"><span data-stu-id="da60e-135">Existing on either the server or the client.</span></span>

<span data-ttu-id="da60e-p106">Los cursores de sólo lectura ayudan a los usuarios a examinar el conjunto de resultados, mientras que los cursores de lectura y escritura permiten implementar actualizaciones en filas individuales. Es posible definir cursores complejos mediante conjuntos de claves que apuntan de vuelta a filas de tablas base. Aunque algunos cursores son de sólo lectura y avance, otros se pueden mover hacia adelante y hacia atrás y proporcionar una actualización dinámica del conjunto de resultados, según los cambios realizados por otras aplicaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="da60e-p106">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates. Complex cursors can be defined with keysets that point back to base table rows. While some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</span></span>

<span data-ttu-id="da60e-p107">No todas las aplicaciones necesitan utilizar cursores para obtener acceso a datos o para actualizarlos. Algunas consultas simplemente no requieren actualización directa de filas mediante un cursor. Los cursores deben ser una de las últimas técnicas empleadas para recuperar datos (y, en ese caso, debe elegir el cursor de menor impacto posible). Al crear un conjunto de resultados mediante un procedimiento almacenado, no es posible actualizar el conjunto de resultados mediante métodos de modificación o actualización con cursores.</span><span class="sxs-lookup"><span data-stu-id="da60e-p107">Not all applications need to use cursors to access or update data. Some queries simply do not require direct row updating by using a cursor. Cursors should be one of the last techniques you choose to retrieve data — and then you should choose the lowest impact cursor possible. When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</span></span>

## <a name="concurrency"></a><span data-ttu-id="da60e-143">Concurrencia</span><span class="sxs-lookup"><span data-stu-id="da60e-143">Concurrency</span></span>

<span data-ttu-id="da60e-p108">En algunas aplicaciones multiusuario, es de vital importancia que los datos presentados al usuario final estén lo más actualizados que sea posible. Un ejemplo clásico es el de un sistema de reservas de una línea aérea, donde puede haber muchos usuarios que deseen el mismo asiento en un vuelo determinado (y, por tanto, un único registro). En estos casos, el diseño de la aplicación debe controlar las operaciones simultáneas en un registro.</span><span class="sxs-lookup"><span data-stu-id="da60e-p108">In some multi-user applications it is vitally important for the data presented to the end user to be as current as possible. A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and thus, a single record). In a case like this, the application design must handle concurrent operations on a single record.</span></span>

<span data-ttu-id="da60e-p109">En otras aplicaciones, la concurrencia no es tan importante. En tales casos, no se justifica el gasto de recursos para mantener los datos actualizados en todo momento.</span><span class="sxs-lookup"><span data-stu-id="da60e-p109">In other applications, concurrency is not as important. In such cases, the expense involved in keeping the data current at all times cannot be justified.</span></span>

## <a name="position"></a><span data-ttu-id="da60e-149">Posición</span><span class="sxs-lookup"><span data-stu-id="da60e-149">Position</span></span>

<span data-ttu-id="da60e-p110">Asimismo, un cursor realiza un seguimiento de la posición actual en un conjunto de resultados. Piense en la posición de un cursor como un puntero al registro actual (es similar a la forma en que un índice de una matriz apunta a su valor asociado dentro de esa matriz).</span><span class="sxs-lookup"><span data-stu-id="da60e-p110">A cursor also keeps track of the current position in a result set. Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</span></span>

## <a name="scrollability"></a><span data-ttu-id="da60e-152">Capacidad de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="da60e-152">Scrollability</span></span>

<span data-ttu-id="da60e-153">El tipo de cursor que usa una aplicación también afecta a la capacidad de avanzar o retroceder por las filas de un conjunto de resultados; este proceso se denomina a veces capacidad de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="da60e-153">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes called scrollability.</span></span> <span data-ttu-id="da60e-154">La capacidad para mover hacia delante *y* hacia atrás a través de un conjunto de resultados agrega a la complejidad del cursor y, por lo tanto, es más costosa de implementar.</span><span class="sxs-lookup"><span data-stu-id="da60e-154">The ability to move forward *and* backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</span></span> <span data-ttu-id="da60e-155">Por ello, sólo debe pedir un cursor con esta funcionalidad cuando sea estrictamente necesario.</span><span class="sxs-lookup"><span data-stu-id="da60e-155">For this reason, you should ask for a cursor with this functionality only when necessary.</span></span>

