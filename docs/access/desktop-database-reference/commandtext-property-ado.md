---
<<<<<<< Título HEAD: CommandText (propiedad) (ADO) TOCTitle: CommandText (propiedad) (ADO) === título: CommandText (propiedad, ADO) TOCTitle: CommandText (propiedad, ADO)
>>>>>>> Master ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID: ms.date 48543234: 18/09/2015 mtps_version: Office.15 f1_keywords:
- ado210.chm1231123 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="commandtext-property-ado"></a>CommandText (propiedad, ADO)
=======
# <a name="commandtext-property-ado"></a>CommandText (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el texto de un comando que se va a emitir en un proveedor.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String** que contiene un comando de proveedor, como una instrucción SQL, un nombre de tabla, una dirección URL relativa o una llamada a un procedimiento almacenado. El valor predeterminado es "" (cadena de longitud cero).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **CommandText** para establecer o devolver el texto de un comando representado por un objeto [Command](command-object-ado.md). Normalmente es una instrucción SQL, pero también puede ser cualquier otro tipo de instrucción de comando que reconozca el proveedor, como una llamada a un procedimiento almacenado. El procesador de consultas del proveedor debe admitir el dialecto o la versión de la instrucción SQL.

<<<<<<< HEAD si la propiedad [Prepared](prepared-property-ado.md) del objeto **Command** se establece en **True** y el objeto **Command** está enlazado a una conexión abierta cuando se establece la propiedad **CommandText** , ADO preparará la consulta () es decir, una forma compilada de la consulta que se almacena por el proveedor) cuando se llama a los métodos [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) u **Open** .
=== Si la propiedad [Prepared](prepared-property-ado.md) del objeto **Command** se establece en **True** y el objeto **Command** está enlazado a una conexión abierta cuando se establece la propiedad **CommandText** , ADO preparará la consulta (es decir, una forma compilada de la consulta que se almacena por el proveedor) cuando se llama a los métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) u **Open** .
>>>>>>> master

Dependiendo del valor de la propiedad [CommandType](commandtype-property-ado.md), puede que ADO modifique la propiedad **CommandText**. La propiedad **CommandText** se puede leer en cualquier momento para ver el texto real del comando que ADO va a utilizar durante la ejecución.

Utilice la propiedad **CommandText** para establecer o devolver una dirección URL relativa que especifica un recurso, como un archivo o un directorio. El recurso es relativo a una ubicación especificada explícitamente por una dirección URL absoluta o implícitamente por un objeto [Connection](connection-object-ado.md) abierto.


> [!NOTE]
<<<<<<< HEAD
> <P>[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</P>
=======
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).
>>>>>>> master


