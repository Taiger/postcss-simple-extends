# postcss-simple-include

Use `@extends` with basic CSS classes instead of mixins.

## Usage

This input:

    .colors {
        background-color: white;
        color: black;
    }

    .padding {
        padding: 1rem 0;
    }

    main {
        @extends .colors;
        @extends .padding;
    }

Will generate into:

    .colors {
        background-color: white;
        color: black;
    }

    .padding {
        padding: 1rem 0;
    }

    main {
        background-color: white;
        color: black;
        padding: 1rem 0;
    }

This syntax is supported too:

    main {
        @extends .colors, .padding;
    }

## License

MIT.
Credit brechtcs/postcss-simple-include
