---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483793"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="5ed62-102">Using the Command Object (Access)</span><span class="sxs-lookup"><span data-stu-id="5ed62-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="5ed62-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ed62-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ed62-p101">Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="5ed62-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="5ed62-p102">Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="5ed62-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="5ed62-p103">No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.</span><span class="sxs-lookup"><span data-stu-id="5ed62-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5ed62-p104">Algunos objetos <STRONG>Command</STRONG> pueden devolver un conjunto de resultados como una secuencia binaria o un único <STRONG>registro</STRONG>, en vez de un objeto <STRONG>Recordset</STRONG>, si el proveedor admite esa posibilidad. Además, algunos objetos <STRONG>Command</STRONG> no devuelven ningún conjunto de resultados (por ejemplo, una consulta Update de SQL). Este capítulo tratará el escenario más típico: ejecutar objetos <STRONG>Command</STRONG> que devuelven resultados en un objeto <STRONG>Recordset</STRONG>. Para obtener más información acerca de los resultados devueltos en objetos <STRONG>Record</STRONG> o <STRONG>Stream</STRONG>, vea <A href="chapter-10-records-and-streams.md">Capítulo 10: Objetos Record y Stream</A>.</span><span class="sxs-lookup"><span data-stu-id="5ed62-p104">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider. Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query). This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object. For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


