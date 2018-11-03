---
title: Qué se puede hacer con ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02fd4c5dc5c44e15d8318653bbef9755899d61f6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947794"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="4c4ad-102">¿Qué se puede hacer con ADO</span><span class="sxs-lookup"><span data-stu-id="4c4ad-102">What you can do with ADO</span></span>


<span data-ttu-id="4c4ad-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c4ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c4ad-p101">ADO se ha diseñado para proporcionar a los programadores un modelo de objetos lógico y eficaz para el acceso, modificación y actualización, mediante código de programación, de una gran variedad de orígenes de datos por medio de interfaces de sistema OLE DB. El uso más común de ADO es el de consultar en una o varias tablas de una base de datos relacional, recuperar y mostrar los resultados en una aplicación y, quizá, permitir a los usuarios que realicen y guarden cambios en los datos. Otras acciones que se pueden realizar mediante programación con ADO son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c4ad-p101">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces. The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data. Other things that can be done programmatically with ADO include:</span></span>

  - <span data-ttu-id="4c4ad-107">Consultar una base de datos mediante SQL y mostrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-107">Querying a database using SQL and displaying the results.</span></span>

  - <span data-ttu-id="4c4ad-108">Obtener acceso a información ubicada en un almacén de archivos a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-108">Accessing information in a file store over the Internet.</span></span>

  - <span data-ttu-id="4c4ad-109">Manipular mensajes y carpetas en un sistema de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-109">Manipulating messages and folders in an e-mail system.</span></span>

  - <span data-ttu-id="4c4ad-110">Guardar los datos de una base de datos en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-110">Saving data from a database into an XML file.</span></span>

  - <span data-ttu-id="4c4ad-111">Permitir a un usuario revisar y realizar cambios en datos de tablas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-111">Allowing a user to review and make changes to data in database tables.</span></span>

  - <span data-ttu-id="4c4ad-112">Crear y volver a usar comandos de base de datos parametrizados.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-112">Creating and reusing parameterized database commands.</span></span>

  - <span data-ttu-id="4c4ad-113">Ejecutar procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-113">Executing stored procedures.</span></span>

  - <span data-ttu-id="4c4ad-114">Crear dinámicamente una estructura flexible, denominada **Recordset**, para contener, manipular datos y navegar por ellos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

  - <span data-ttu-id="4c4ad-115">Realizar operaciones transaccionales de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-115">Performing transactional database operations.</span></span>

  - <span data-ttu-id="4c4ad-116">Filtrar y ordenar copias locales de información de base de datos según criterios especificados en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

  - <span data-ttu-id="4c4ad-117">Crear y manipular resultados jerárquicos de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-117">Creating and manipulating hierarchical results from databases.</span></span>

  - <span data-ttu-id="4c4ad-118">Enlazar campos de base de datos a componentes diseñados para datos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-118">Binding database fields to data-aware components.</span></span>

  - <span data-ttu-id="4c4ad-119">Crear **conjuntos de registros** desconectados remotos.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="4c4ad-p102">ADO debe exponer una gran variedad de opciones y valores de configuración para proporcionar dicha flexibilidad. Por lo tanto, es importante adoptar un enfoque metódico para aprender a utilizar ADO en una aplicación, descomponiendo cada uno de sus objetivos en partes manejables.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-p102">ADO must expose a wide variety of options and settings in order to provide such flexibility. Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="4c4ad-p103">En la mayoría de los programas ADO existen cuatro operaciones principales implicadas: obtener, examinar, modificar y actualizar datos. Los siguientes cuatro capítulos describen cada una de estas operaciones con más detalle.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-p103">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data. The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="4c4ad-p104">Antes de continuar, familiarícese con los objetos del Modelo de objetos ADO. A continuación, revise [HelloData: una aplicación ADO sencilla](hellodata-a-simple-ado-application.md). Esta aplicación está escrita en Visual Basic y realiza cada una de las cuatro operaciones principales de ADO.</span><span class="sxs-lookup"><span data-stu-id="4c4ad-p104">Before proceeding, familiarize yourself with the objects in the ADO Object Model. Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md). This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

